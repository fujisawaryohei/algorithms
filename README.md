### Search algorithm
## LinearSearch algorithm with Ruby
```
def linear_search(searchArr,searchNum)
  index = 0
  count = 0
  searchArr.each do |arr|
    if arr == searchNum
      count += 1
    else
      index += 1
    end
  end
  if count == 0
    puts "value:#{searchNum} Array:#{searchArr} There isn't it."
  else
    puts "value:#{searchNum} Array:#{searchArr} There is it at index\s#{index}."
  end
end
```

## BinarySearch algorithm with Ruby
```
def binary_search(array,searchNum)
  array.sort!
  leftIndex = 0
  rightIndex = array.index(array.last)
  midIndex = (rightIndex + leftIndex) / 2
  loop do
    if searchNum == array[midIndex]
      # puts "Array->#{array}:There is at #{midIndex}!"
      break;
    elsif searchNum > array[midIndex]
      midIndex += 1
    else
      midIndex -= 1
    end
  end
end
```

### Sort algorithm
## BubbleSort algorithm with Ruby
```
def bubble_sort(array)
  arrayLength = array.length
  for length in 1..arrayLength  #要素のインデックスをlに入れる
    for nextIndex in 1..(arrayLength - length) #
      if array[nextIndex-1] > array[nextIndex]
        t = array[nextIndex-1]
        array[nextIndex-1] = array[nextIndex]
        array[nextIndex] = t
      end
    end
  end
  p array
end
```
