---
title: Merge Sort Algo in Ruby
date: 2019-04-21 10:26:00 -05:00
tags:
- ruby
- mergesort
- merge
- sort
---

```ruby
def merge_sort(arr)

if arr.length <= 1
arr
else
mid = (arr.length/2).floor
left = merge_sort(arr\[0..mid - 1\])
right = merge_sort(arr\[mid..arr.length\])
merge(left, right)
end

end

def merge(left, right)
if left.empty?
right
elsif right.empty?
left
elsif left.first < right.first
\[left.first\] \+ merge(left\[1..left.length\], right)
else
\[right.first\] \+ merge(left, right\[1..right.length\])
end

end
```