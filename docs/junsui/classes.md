---
title: คลาส
# description: dolor sit amet
# icon: material/emoticon-happy
# status: new
# status: deprecated
# subtitle: Nullam urna elit, malesuada eget finibus ut, ac tortor
---

<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </p>

<figure markdown="span">
  ![Classes](\imgs\class.png){ width="800" }
</figure>

## อาวุธไมนด์

ประเภทอาวุธไมนด์กับคลาสของจุนซุยผู้เป็นเจ้าของจะต้องสอดคล้องกัน อาวุธบางอย่างมีความก้ำกึ่งระหว่างคลาส หรือบางครั้งมีรูปแบบการใช้ที่ข้ามคลาสซึ่งไม่อนุญาตให้สามารถทำได้

การออกแบบอาวุธของขั้นต้นจำเป็นต้องมีรายละเอียด, ขนาดของอาวุธ, ความสามารถต่าง ๆ รวมถึงภาพประกอบเพื่อความสะดวกในการโรล สามารถนำอาวุธที่มีอยู่จริงบนโลกหรือตำนานมาใช้ได้

สำหรับอาวุธที่มีฟังก์ชั่นหลักมากกว่า 1 จะถูกบังคับให้อยู่คลาสอิรุกะ และหากอาวุธใดมีกลไกพิเศษทีมงานจะพิจารณาว่ามีความเป็นไปได้ในการสร้างหรืออนุโลมให้ได้หรือไม่ หากทีมงานถามจะต้องตอบได้ว่ากลไกเหล่านั้นทำงานได้อย่างไร สร้างความเสียหายได้ในระดับไหน เป็นต้น

???+ failure "ตัวอย่างการเลือกไมนด์และคลาสที่ผิด"

    ปืนพก คลาสไลออน
    > ถึงแม้จะใช้ปืนต่อสู้ในระยะประชิดได้ แต่อาวุธข้ามสาย จึงให้ผ่านไม่ได้

    ปืนติดดาบ คลาสทากะ/ไลออน
    > ถือว่ามีฟังก์ชั่นมากกว่า 1 (ยิงและฟัน) ถือว่าเป็นอาวุธสายอิรุกะ

    อาวุธสร้างแบล็คโฮล คลาสอิรุกะ
    > ปัจจุบันยังไม่สามารถสร้างแบล็คโฮลได้ หรืออาจสร้างได้แล้วแต่ควบคุมไม่ได้ จึงไม่อนุญาตให้ผ่าน



???+ warning "ตัวอย่างการเลือกไมนด์และคลาสที่คลุมเครือ"

    เคียวยักษ์ (ไลออน/ไซ)
    > โดยปกติแล้วเคียวเป็นอาวุธที่มีความหนักมาก ไลออนจึงไม่สามารถถือมันกวัดแกว่งอย่างคล่องแคล่วได้ ผู้ใช้จึงต้องอยู่ในคลาสไซ

    เลื่อย (ไลออน/ไซ)
    > หากต้องการเล่นคลาสไลออน ต้องใช้เลื่อยตัวเล็กที่มีน้ำหนักเบาและความคล่องตัวสูงกว่า แต่หากต้องการใช้เลื่อยตัวใหญ่ต้องเป็นคลาสไซ

    ปืนใหญ่ (ไซ/ทากะ)
    > พื้นฐานของปืนใหญ่คืออาวุธระยะไกล ต่อให้จะถือปืนใหญ่ไปฟาดหรือต้องใช้แรงมาก ๆ ในการขนย้าย ก็ต้องเป็นคลาสทากะอยู่ดี

    ไม้จิ้มฟัน
    > หากจะวิ่งถือไม้จิ้มฟันไปจิ้มตาศัตรูก็เป็นไลออน หากใช้ปาก็เป็นทากะ หากเป็นเฮบิก็สามารถออกแบบพลังพิเศษให้ไม้จิ้มฟันได้ แต่เป็นไซไม่ได้เพราะไม้จิ้มฟันมีน้ำหนักเบา เป็นอิรุกะก็ไม่ได้เพราะไม่ได้มีกลไกอะไร

---

ตั้งแต่เริ่มจุนซุยทุกคนจะมีคลาสตามอาวุธและแนวทางการต่อสู้เริ่มต้นของตนเองซึ่งไม่สามารถเปลี่ยนแปลงได้ แต่ละคลาสจะมีจุดเด่นจุดด้อยที่ต่างกัน และจะมีค่าสเตตัสพิเศษ (บัพคลาส) ที่เพิ่มให้ไม่เหมือนกันด้วย

=== "ไลออน (Lion)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Str +20% | Dex +15% | Agi +15%

    * ไลออนมีสมรรถนะทางกายที่รวดเร็วและความคล่องตัวที่สูง สามารถเคลื่อนที่ได้อย่างเหลือเชื่อกว่าคลาสอื่น ๆ ราวกับราชสีห์ที่ไล่ล่าเหยื่อด้วยความสง่างาม
    * ใช้อาวุธจำพวกอาวุธที่ดูคล่องตัว เคลื่อนไหวสะดวก และโจมตีระยะสั้น เช่น ดาบ หอก มีด มีดสั้น สนับมือ กรงเล็บ แส้
    * สำหรับในขั้นต้น ไลออนจะยังไม่มีสกิลหรือความสามารถพิเศษ

=== "ทากะ (Taka)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Agi +10% | Dex +40%

    * ถนัดการต่อสู้ระยะไกล มีประสาทสัมผัสที่แม่นยำ สามารถรับรู้สถานการณ์รอบตัวที่เกิดขึ้นได้อย่างกว้างขวางและตื่นตัวกับสถานการณ์รอบ ๆ ตลอดเวลาเพื่อตั้งรับและโจมตีในเวลาเดียวกัน มองเห็นและอ่านเกมขาดอยู่เสมอ ดั่งเหยี่ยวที่โบยบินบนฟากฟ้า และทอดสายตามองสนามรบอย่างชัดแจ้ง
    * ใช้อาวุธจำพวกอาวุธประเภทโจมตีระยะไกล/กลาง เช่น ปืน ธนู หน้าไม้
    * สำหรับในขั้นต้น ทากะจะยังไม่มีสกิลหรือความสามารถพิเศษ

=== "ไซ (Sai)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Str +40% | Vit +20%

    * พละกำลังที่มหาศาล  ความอึดและกล้ามเนื้อที่แข็งแกร่ง ไซเป็นแนวหน้าให้แก่ทีม และเป็นกำแพงอันแข็งแกร่งผู้คอยรับการโจมตีหรือปกป้องเพื่อนร่วมทีม หรือจะบุกทะลวงชนดุจดั่งแรดที่ทรงพลัง
    * มีอาวุธจำพวกอาวุธที่น้ำหนักมาก เช่น ค้อน ง้าว ทวน เคียว
    * สำหรับในขั้นต้น ไซจะยังไม่มีสกิลหรือความสามารถพิเศษ

=== "อิรุกะ (Iruka)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Agi +30% | Vit +20%

    * ความพิเศษจะต่างจากคลาสอื่น ๆ ที่ไม่มีความเก่งกาจในด้านใดเป็นพิเศษ ไมนด์ของอิรุกะนั้นมีความหลากหลายในด้านการใช้งาน สามารถปรับเปลี่ยนลักษณะรูปแบบของตัวเองให้ใช้ได้ในสถานการณ์ที่หลากหลาย เปรียบดั่งปลาโลมาที่พลิ้วไหวในสายน้ำ และยังมีความฉลาดที่คอยเป็นไหวพริบให้กับตนอยู่เสมอ
    * มีอาวุธจำพวกเทคโนโลยี มีกลไกฟังก์ชั่นต่าง ๆ โดยในขั้นแรกสามารถมีรูปแบบให้ปรับเปลี่ยนได้สองโหมด เช่น สามารถปรับเปลี่ยนอาวุธให้เป็นดาบหรือปืน (ไม่สามารถให้ทั้งสองรูปแบบใกล้เคียงกันมากได้ เช่น ดาบ กับดาบที่ยาวกว่า)
    * สำหรับในขั้นต้น นอกจากการปรับเปรี่ยนรูปลักษณ์แล้วอิรุกะจะยังไม่มีสกิลหรือความสามารถพิเศษ

=== "เฮบิ (Hebi)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Agi +10% | Int +15%

    * มีความสามารถของในด้านสกิลที่เป็นลักษณะของแอสแซสซิน วางกับดัก หรือสร้างเงื่อนไขต่าง ๆ ในการดีบัพใส่ศัตรู เหมือนกับนักล่าที่วางกับดัก และคอยต้อนเหยื่อให้จนมุมด้วยเทคนิคทุกอย่างที่ตนมีเพื่อปลิดชีพเหยื่ออย่างแม่นยำ ==เป็นคลาสเดียวที่ให้เกิดดีบัพการติดสถานะผิดปกติต่าง ๆ โดยตรงได้ เช่น ลดสเตตัส==
    * ไมนด์ของคลาสนี้มีลักษณะเป็นชุด เช่น ซองมีดสั้นจำนวนหนึ่ง สำรับไพ่ ระเบิด กับดัก หรืออาวุธชนิดต่าง ๆ ที่ต้องใช้ในจำนวนมากเพื่อควบคุมมัน และใช้ในการโจมตี หรือเป็นอาวุธที่มีความพิเศษและพิสดาร แต่ก็มีเงื่อนไขการใช้งานที่ยุ่งยากเพื่อแลกกับความพิเศษของมัน
    * คลาสเฮบิในขั้นแรกอนุญาตให้มีความสามารถพิเศษตั้งแต่ขั้นแรก (อ่านเพิ่มเติมในเรื่องขอบเขตการเขียนสกิล)

    !!! danger ""

        ไม่แนะนำสถานะที่ตีความระดับความเสียหายให้ตรงกันได้ยาก เช่น เลือดไหล, ติดพิษ, ฯลฯ

=== "โคโจ (Kochou)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Vit +15% | Int +20%

    * โคโจเป็นคลาสที่มีความสามารถที่โดดเด่นในการรักษาบาดแผลหรือว่าบัพสถานะต่าง ๆ และคอยซัพพอร์ต อาจสร้างโล่ป้องกันหรือคอยสร้างจังหวะให้กับทีม เป็นแนวหลังของปาร์ตี้ที่จะคอยโอเปอเรททีมอยู่เสมอ หรือก็คือกำแพงแห่งแนวหลังนั้นเอง
    * ไมนด์ของคลาสโคโจนั้นก็คือพวกเครื่องรางของขลังต่าง ๆ หรือเครื่องดนตรี
    * ข้อเสียของคลาสนี้คือเป็นคลาสที่ไม่โดดเด่นในเรื่องการโจมตี (มีสกิลโจมตีได้บ้างแต่ไม่รุนแรง) ปกติจึงเน้นการสนับสนุนให้เพื่อนทำดาเมจแทน
    * ไม่สามารถมี Second Mind เมื่อเลื่อนขั้นจะมีจำนวนสกิลและขอบเขตสกิลเพิ่มขึ้น แต่ยังสามารถมี Over Mind ได้

    !!! note "สกิลเฉพาะของโคโจ"

        เนื่องจากรูปแบบการเล่นของโคโจมีความพิเศษ จึงมีสกิลเฉพาะให้เพื่อให้โคโจมีบทบาทมากขึ้น
        รายละเอียดเพิ่มเติม: [สกิลเฉพาะของโคโจ (Connector)]()
        <!-- TODO: link -->

=== "คุจากุ (Kujaku)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Dex +10% | Int +30%

    * คุจากุเป็นคลาสของจุนซุยที่เพิ่งมีการคิดค้นขึ้น มีความสามารถดั่งเวทมนต์ที่ไร้ขอบเขต สามารถควบคุมธาตุต่าง ๆ ได้ (เช่น ดิน, น้ำ, ลม, ไฟ, สายฟ้า, แสง, มืด, ไม้) หรือจะเป็นวัตถุต่าง ๆ สสารต่าง ๆ สภาพอากาศ แรงโน้มถ่วง จะเป็นความสามารถเหมือนดั่งพลังจิต
    * ไมนด์ของคุจากุจะเป็นเพียงแค่เครื่องประดับติดตัว แต่พลังจะส่งออกมาแก่ผู้ใช้โดยตรง สามารถควบคุมการโจมตีด้วยมือได้อย่างอิสระ (แต่คลาสนี้สามารถลงได้เฉพาะเขตนางาซากิ)
    * ข้อเสียของคลาสนี้คือ ไม่สามารถบัพตัวเองได้ ต้องอาศัยการบัพจากคลาสโคโจเท่านั้น
    * ไม่สามารถมี Second Mind, Over Mind และ Beyond Mind ได้ แต่เมื่อเลื่อนขั้นจะมีจำนวนสกิลเพิ่มขึ้น และสามารถเพิ่มขอบเขตในการความคุมความสามารถของตนเองได้ และสามารถใช้ Eikonik Mind ได้เมื่อคุจากุไปจึงจุดสูงสุดของจุนซุย หรือ Beyond Master

    !!! danger ""

        คุจากุจะอยู่สังกัดเขตของนางาซากิเท่านั้น ไม่สามารถอยู่เขตอื่นได้

=== "คุโมะ (Kumo)"

    <figure markdown="span">
      ![Image title](https://dummyimage.com/600x400/){ width="300" }
      <figcaption>Image caption</figcaption>
    </figure>

    > ค่าสเตตัสพิเศษ: Vit +50%

    * คุโมะเป็นคลาสที่แตกต่างจากจุนซุยทั้งหมดโดยสิ้นเชิง เพราะความสามารถทั้งหมดของคลาสนี้จะมาจากพลังงานด้านลบ หากไม่นับโคโจที่เด่นเรื่องการสนับสนุนแล้วคุโมะสามารถบัพค่าสเตตัสทุกอย่างให้กับตัวเองได้สูงที่สุด และอิสระที่สุด โดยรวมคุโมะคือคลาสสำหรับการบุกทะลวงฟันและโจมตีอย่างบ้าคลั่ง
    * เนื่องจากเป็นคนที่ตายขณะที่ตนเองก็มีอินไซเดอร์อยู่ในตัวทำให้ไม่สามารถมีไมนด์ลักษณะเดียวกับคนอื่นได้ พวกเขาจึงต้องเอาอินไซเดอร์ของตนมาใช้เป็นอาวุธแทน โดยพวกเขาจะมีถุงมือลวดลายต่าง ๆ ที่ใช้ในการควบคุมแทนไมนด์ หากหมดสติอินไซเดอร์จะสลายกลับเข้าถุงมือไป โดยถุงมือนี้จะมีคุณสมบัติคล้ายไมนด์ แต่จะควบคุมความสามารถทั้งหมดด้วยพลังงานด้านลบ
    * ข้อเสียของคลาสนี้คือ ตัวอินไซเดอร์ไม่สามารถรับบัพ/ฮีลจากจุนซุยด้วยกันได้เนื่องจากใช้พลังงานขั้วตรงข้ามกัน และหากตัวจุนซุยได้รับการล้างสถานะ สถานะการเชื่อมต่อพลังจะถูกตัดออกชั่วคราว ทำให้อินไซเดอร์กลับเข้าไปอยู่ถุงมือ
    * ไม่สามารถมี Second Mind และ Over Mind ได้ แต่เมื่อเลื่อนขั้นจะมีจำนวนสกิลเพิ่มขึ้น และสามารถเพิ่มขอบเขตในการความคุมความสามารถของตนเองได้
    * นอกจากนี้เมื่อคุโมะต่อสู้ จะโอนค่าสเตตัสทั้งหมดไปยังอินไซเดอร์เพื่อให้จู่โจมแทน (ลดค่าสเตตัสทั้งหมดจนเหลือ B) สกิลทั้งหมดจะอยู่ที่อินไซเดอร์ กล่าวคือตัวจุนซุยจะทำได้เพียงออกคำสั่งเท่านั้น

    !!! danger ""

        * คุโมะจะอยู่สังกัดเขตของชิบุย่าเท่านั้น ไม่สามารถอยู่เขตอื่นได้
        * อินไซเดอร์ที่คุโมะควบคุมไม่สามารถรับบัพ/ฮีลได้
        * เมื่อเรียกอินไซเดอร์กลับเข้าถุงมือ จะมีคูลดาวน์การเรียกใหม่ 1 เทิร์น