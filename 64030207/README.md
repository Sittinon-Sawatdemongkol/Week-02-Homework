# 64030161 Rachata Supanurak

1. สร้าง component LED ใน project 1

![Screenshot 2566-07-16 at 01 36 41](https://github.com/RachataS/Week-02-Homework/assets/115066261/cb45e3cd-3c3b-4e71-a4ba-2e234478730f)

2. แก้ไขไฟล์ LED.h ใน component

```css
void ON(pin);
void OFF(pin);
```

3. แก้ไขไฟล์ LED.c ใน component

```css
#include <stdio.h>
#include "LED.h"
#include "driver/gpio.h"

void ON(int pin)
{
    gpio_set_level(pin, 1);
}
void OFF(int pin)
{
    gpio_set_level(pin, 0);
}
```
4. แก้ไขไฟล์ CMakeLists.txt 
```css
idf_component_register(SRCS "LED.c"
                       INCLUDE_DIRS "include")
```

5. push project 1 ขึ้น github
6. สร้าง project 2
7. สร้าง ไฟล์ idf_component.yml และแก้ไขดังนีเพื่อให้สามารถเรียกใช้งาน component จาก github ได้
```css
targets:
  - esp32
description: component example of esp32
dependencies:
  LED_class:
    git: https://github.com/RachataS/IOT_W2.git //เลือก repo mี่ต้องการเรียกใช้ component
    path: components/LED //เลือก path ของ component

```
8. build project เพื่อ clone component ลงมาที่ project ของเรา
9. แก้ไข code ใน main.c เพื่อเรียกใช้ component

# URL

1. project ข้อ 1 = https://github.com/RachataS/IOT_W2.git
2. project ข้อ 4 = https://github.com/RachataS/IOT_W2.2.git
