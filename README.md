#ใบงานที่ 6 เรื่อง การใช้งานคำสั่ง Console.Read() และ Console.ReadLine()

# นาย ชาตรี พรหมประเสริฐ 57030160

##วัตถุประสงค์
1). เพื่อให้นักศึกษาบอกชื่อ method ที่ใช้ในการรับค่าตัวอักษรพื้นฐานในภาษา C# ได้

2). เพื่อให้นักศึกษาสามารถใช้คำสั่งรับค่าตัวอักษรได้
##ความรู้เบื้องต้น
คำสั่งที่ใช้รับค่าตัวอักษรทางอินพุตมาตรฐานของ C# คือ ```Console.Read()``` และ ``` Console.ReadLine()``` โดยทั้งสองจะมีข้อแตกต่างกันคือ ```Read()``` จะอ่านตัวอักษร ส่วน ```ReadLine()``` จะอ่านสตริง จนกว่าจะกด Enter ในการรับค่าด้วย ```Read()``` และ ```ReadLine()``` จะรับเฉพาะค่า ASCII เท่านั้น หากต้องการรับค่าตัวเลข จะต้องมีการแปลง ASCII ของตัวเลขที่พิมพ์เข้ามาให้เป็นค่าตัวเลข (การรับอักษร “22” จะไม่ได้หมายถึงค่าตัวเลข 22) 

##ลำดับขั้นการทดลอง

1). สร้าง Project ตั้งชื่อเป็น Lab6 เพื่อทดลองการใช้งานคำสั่ง ```Console.ReadLine()``` และ ```Console.ReadLine()```

2). โปรแกรมสำหรับรับตัวอักษรจากคีย์บอร์ด 

  2.1). แก้ไขโปรแกรมให้เป็นดังรูป

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic1.png)

  2.2).	โปรแกรม และบันทึกผลที่ได้


ผลของโปรแกรมคือ ![](https://github.com/est160/LAB-06/blob/master/imgs/lab%2061.png?raw=true)


###คำถาม 6.1 ถ้าพิมพ์ตัวอักษรจำนวนหลายๆ ตัวแล้วกด Enter จะได้ผลอย่างไร ทำไมจึงเป็นเช่นนั้น


จะได้แค่ตัวอักษรแค่ตัวแรกเพราะ char สามารถแสดงอักษรออกมาได้ 1 ตัว


###คำถาม 6.2 ในบรรทัดที่ 11 ซึ่งมีโปรแกรมเป็น ```ch = (char)Console.Read();```  นั้น ถ้าตัด ```(char)``` ออกไป จะเกิดอะไรขึ้น ให้อธิบายประกอบ


จะทำให้โปรแกรมไม่สามารถรันได้เพราะโปรแกรมไม่ทราบว่าจะให้นำค่าที่ป้อนเข้ามาแสดงออกเป็นชนิดใดและให้แสดงออกที่ไหน


3).	โปรแกรมสำหรับรับ string จากคีย์บอร์ด
 
 3.1).	แก้ไขโปรแกรมให้เป็นดังรูป

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic2.png)
 
 3.2).	โปรแกรม และบันทึกผลที่ได้


ผลที่ได้จากการรรันโปรแกรมคือ ![](https://github.com/est160/LAB-06/blob/master/imgs/lab%2062.png?raw=true)


4).	โปรแกรมสำหรับรับค่าตัวเลข เนื่องจากคำสั่ง ```Read()``` และ ```ReadLine()``` จะรับเฉพาะตัวอักษร การรับตัวเลข เราต้องใช้เมธอด TryParse() มาช่วยแปลงค่า

4.1).	แก้ไขโปรแกรมให้เป็นดังรูป
 
 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic3.png)

4.2).	รัน โปรแกรม โดยป้อนตัวเลขใดๆ และบันทึกผลที่ได้



ผลที่ได้จากการรันโปรแกรมคือ ![](https://github.com/est160/LAB-06/blob/master/imgs/lab%2063.png?raw=true)


###คำถาม 6.3 ถ้าเราป้อนตัวอักษรลงไปแทนที่ตัวเลข จะเกิดอะไรขึ้น มีวิธีการป้องกันหรือแก้ไขอย่างไร


เกิด error แก้ไขโดยใช้ประโยค try{…} catch{…}


5).	โปรแกรมสำหรับรับค่าตัวเลข แต่ในบางกรณีที่ผู้ใช้ป้อนตัวอักษร จะทำให้เกิด error และทำให้โปรแกรม hang ได้ จึงต้องมีการป้องกันโดยใช้ประโยค ```try{…} catch{…}```  (ประโยค ```try{…} catch{…}``` นี้จะศึกษารายละเอียดภายหลัง)

  5.1).	แก้ไขโปรแกรมให้เป็นดังรูป

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-06/blob/master/imgs/pic4.png)

  5.2).	รัน โปรแกรม โดยป้อนตัวเลขใดๆ และบันทึกผลที่ได้


ผลที่ได้จากการรันคือ ![](https://github.com/est160/LAB-06/blob/master/imgs/lab%2064.png?raw=true)


###คำถาม 6.4 ถ้าเราป้อนตัวอักษรลงไปแทนที่ตัวเลข จะเกิดอะไรขึ้น เหมือนหรือต่างจากโปรแกรมก่อนหน้านี้อย่างไร


รันได้แต่มีการแจ้งเตือนการเกิด error แต่โปรแกรมจะมีการแจ้งเตือนว่าระบบไม่สามารถใช้ค่าตัวอักษรได้



##แบบฝึกหัด ให้เขียน code ในการรับค่าอินพุตต่อไปนี้และแสดงออกหน้าจอให้ถูกต้อง
``` Name :  (ป้อนชื่อของนักศึกษา). ```

``` Lastname : (ป้อนนามสกุลนักศึกษา).```

``` ID : (ป้อนรหัสนักศึกษา).```

``` GPA : (ป้อนเกรดเฉลี่ยนักศึกษา โดยมีทศนิยมสองหลัก).```


using System;

namespace lab_6
{
    class Program
    {
        static void Main(string[] args)
        {
            

                Console.Write("Name :");
                string val1 = Convert.ToString(Console.ReadLine());
                
                Console.Write("Lastname:");
                string val2 = Convert.ToString(Console.ReadLine());
                
                Console.Write("ID:");
                int val3 = Convert.ToInt32(Console.ReadLine());
                
                Console.Write("GPA:");
                string val4 = Convert.ToString(Console.ReadLine());

               
                Console.WriteLine("Name " + val1);
                Console.WriteLine("Lastname " + val2);
                Console.WriteLine("ID " + val3);
                Console.WriteLine("GPA " + val4);
            
        }
    }
}


ผลที่ได้คือ 

![](https://github.com/est160/LAB-06/blob/master/imgs/lab65.png?raw=true)
