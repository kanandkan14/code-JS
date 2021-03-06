# Code Kata
---
A code kata is an exercise in programming which helps programmers hone their skills through practice and repetition. ~ Wiki

# How to run test
## JS
- Go to js directory
- Install libraries 
```
  $ npm install
```
- Testing with Jest
```
  $(npm bin)/jest week1
```

## Ruby
- Go to ruby directory
- Install libraries
```
  $ bundle install
```

- Testing with minitest
```
  $ ruby week1/test.rb
```

# Week 1
## Set Alarm (set_alarm)
สร้างงฟังก์ชัน `set_alarm` ซึ่งรับพารามิเตอร์ 2 ตัว คือ employed และ vacation โดยจะมีการคืนค่าผลลัพธ์ตามเงื่อนไขต่อไปนี้ 
- ฟังก์ชันจะคืนค่าผลลัพธ์เป็นจริง เมื่อพารามิเตอร์ employed เป็นจริง และ vacation เป็นเท็จ
- นอกเหนือจากเงื่อนไขข้างต้น จะให้ผลลัพท์เป็นเท็จ

### Example
```
  set_alarm(true, true) → false
  set_alarm(false, true) → false
  set_alarm(true, false) → true
```

### Assertion
```
  assert_equal set_alarm(true, true), false
  assert_equal set_alarm(false, true), false
  assert_equal set_alarm(false, false), false
  assert_equal set_alarm(true, false), true
```
---

## Reverse Order (reverse_order)
สร้างฟังก์ชัน `reverse_order` ซึ่งรับพารามิเตอร์ 1 ตัวเป็น array ของตัวเลข และให้ทําการคืนค่าผลลัพธ์เป็น array ชุดใหม่ที่ได้เรียงลำดับย้อนหลัง

*** ห้ามใช้ฟังก์ชัน built-in ของ Array

### Example
```
  reverse_order([1,2,3,4]) == [4,3,2,1]
  reverse_order([3,1,5,4]) == [4,5,1,3]
```

### Assertion
```
  assert_equal(reverse_order([9,7,2,1,5]), [5,1,2,7,9])
  assert_equal(reverse_order([8,6,5,4,1,3]), [3,1,4,5,6,8])
```
---

## Count positives/Sum negatives(count_positives_sum_negatives)
สร้างฟังก์ชัน `count_positives_sum_negatives` ซึ่งรับพารามิเตอร์ 1 ตัวเป็น array ของตัวเลข
และทําการคืนค่าผลลัพท์เป็น array ที่ประกอบไปด้วยจํานวนนับของตัวเลขที่เป็นค่าบวกในตําแหน่งที่ 1 และผลรวมของตัวเลขที่เป็นค่าลบในตําแหน่งที่ 2
ถ้าพารามิเตอร์ที่รับเป็นค่าว่างหรือ null ให้ทําการคืนค่าเป็น array ว่าง

### Example
```
  count_positives_sum_negatives([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15] → [10, -65]
```

### Assertion
```
  assert_equal(count_positives_sum_negatives([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15]), [10, -65])
  assert_equal(count_positives_sum_negatives([0, 2, 3, 0, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14]), [8, -50])
  assert_equal(count_positives_sum_negatives([1]), [1, 0])
  assert_equal(count_positives_sum_negatives([-1]), [0, -1])
  assert_equal(count_positives_sum_negatives([0,0,0,0,0,0,0,0,0]), [0, 0])
```
#   c o d e - J S  
 