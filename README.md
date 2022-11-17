## Installation

### **Install vis_intern library**

To install the base Gym library, use `pip install gym`.

To upgrade vis_intern library, use `pip install --upgrade vis_intern`.

### **Clone github**

`git clone http://ngoxuanphong/vis_intern.git`

## P_state
*   [:6] là **các nguyên liệu đang có trên bàn**
*   [6: 18] **thông tin của người chơi**, gồm có  6 nguyên liệu đang có, 5 nguyên liệu mặc định và điểm
*   [18:102]:   **12 thẻ bình thường trên bàn**, mỗi thẻ có 7 state gồm: [điểm, loại thẻ, 5 nguyên liệu mua]
*   [102: 127]:   **5 thẻ Noble trên bàn**, mỗi thẻ có 5 state gồm: [5 loại nguyên liệu cần]
*   [127:148]:   **3 thẻ úp trên tay**, mỗi thẻ có 7 state gồm: [điểm, loại thẻ, 5 nguyên liệu mua]
*   [148: 153]:  **5 nguyên liệu đã lấy** trong phase lấy nguyên liệu
*   [153:156]: **điểm của 3 người chơi còn lại**
*   [156:159]: **Có thể úp được thẻ ẩn không**, 1 là có, 2 là không. Gồm có 3 thẻ ẩn của 3 loại
*   [159]: **Số thẻ có thể úp trên bàn**

## Action
* [0]   :Là **action bỏ lượt**
* [1:13] **lấy 12 thẻ trên bàn**
* [13:16] Là **mở 3 thẻ đang úp**
* [16:28] Úp **12 thẻ trên bàn**
* [28:31] Úp **3 thẻ ẩn**
* [31:36] Lấy **5 nguyên liêu**
* [36:42] Trả **6 nguyên liệu**


**intern_main('Tên hàm người chơi', số trận, print mode)**

    - *số trận*: là số trận muốn test

    - print mode: True là có in, False là không