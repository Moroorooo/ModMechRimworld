# ModMechRimworld
ModMechRimworld
![image](https://github.com/user-attachments/assets/3025d139-5154-48b7-8c79-28e73bcb34fe)
# ModMechRimworld - Hướng dẫn chỉnh sửa thông số tiêu thụ năng lượng của Mech trong RimWorld

Mod này cho phép bạn chỉnh sửa thông số tiêu thụ năng lượng hàng ngày của Mech (cơ giới) trong game RimWorld. Mặc định, Mech tiêu thụ 10% năng lượng mỗi ngày, nhưng với mod này, bạn có thể thay đổi giá trị này thành bất kỳ con số nào bạn muốn.

## Cài đặt và sử dụng

1. **Tải xuống và cài đặt Mod**:  
   - Tải xuống file XML của mod từ repository này.
   - Đặt file XML vào thư mục Mods của RimWorld. Thư mục Mods thường nằm trong thư mục cài đặt game RimWorld, ví dụ: `RimWorld/Mods/`.

2. **Chỉnh sửa thông số tiêu thụ năng lượng**:  
   - Mở file XML bằng bất kỳ trình soạn thảo văn bản nào (ví dụ: Notepad++, Visual Studio Code, hoặc Notepad).
   - Tìm đến dòng `<defaultBaseValue>0.1</defaultBaseValue>`. Giá trị `0.1` tương ứng với 10% tiêu thụ năng lượng mỗi ngày.
   - Thay đổi giá trị `0.1` thành giá trị bạn mong muốn. Ví dụ, nếu bạn muốn Mech chỉ tiêu thụ 5% năng lượng mỗi ngày, hãy thay đổi thành `0.05`. Nếu bạn muốn Mech tiêu thụ 20% năng lượng mỗi ngày, hãy thay đổi thành `0.2`.

   ```xml
   <StatDef ParentName="MechStatBase">
     <defName>MechEnergyUsageFactor</defName>
     <label>energy usage multiplier</label>
     <description>A multiplier on how fast a mechanoid consumes its energy reserves while operating.</description>
     <defaultBaseValue>0.1</defaultBaseValue> <!-- Thay đổi giá trị này -->
     <minValue>0</minValue>
     <toStringStyle>PercentZero</toStringStyle>
     <displayPriorityInCategory>2000</displayPriorityInCategory>
     <scenarioRandomizable>true</scenarioRandomizable>
     <showIfUndefined>false</showIfUndefined>
   </StatDef>
   ```

3. **Lưu và khởi động lại game**:  
   - Sau khi chỉnh sửa, lưu file XML và khởi động lại RimWorld.
   - Kích hoạt mod trong danh sách Mods của game.

## Ví dụ

- **Giảm tiêu thụ năng lượng**:  
  Nếu bạn muốn Mech chỉ tiêu thụ 5% năng lượng mỗi ngày, hãy thay đổi `<defaultBaseValue>0.1</defaultBaseValue>` thành `<defaultBaseValue>0.05</defaultBaseValue>`.

- **Tăng tiêu thụ năng lượng**:  
  Nếu bạn muốn Mech tiêu thụ 20% năng lượng mỗi ngày, hãy thay đổi `<defaultBaseValue>0.1</defaultBaseValue>` thành `<defaultBaseValue>0.2</defaultBaseValue>`.

## Lưu ý

- **Backup file gốc**: Trước khi chỉnh sửa, hãy sao lưu file XML gốc để tránh các lỗi không mong muốn.
- **Tương thích**: Mod này có thể không tương thích với các mod khác cũng thay đổi thông số của Mech. Hãy kiểm tra kỹ trước khi sử dụng cùng lúc nhiều mod.

## Hỗ trợ

Nếu bạn gặp bất kỳ vấn đề nào hoặc có câu hỏi, vui lòng liên hệ qua repository hoặc để lại issue trên GitHub.

Chúc bạn chơi game vui vẻ!
