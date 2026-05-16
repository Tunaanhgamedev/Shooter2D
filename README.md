# 🔫 Shooter2D: Survival Action Framework

[![Unity Version](https://img.shields.io/badge/Unity-2022.3%20LTS-blue.svg?style=flat-square&logo=unity)](https://unity.com/)
[![Language](https://img.shields.io/badge/Language-C%23-green.svg?style=flat-square&logo=c-sharp)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Genre](https://img.shields.io/badge/Genre-Survivor%20%7C%20Auto--Shooter-red.svg?style=flat-square)](https://unity.com/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg?style=flat-square)](LICENSE)

> Một Framework chuyên sâu cho thể loại trò chơi hành động sinh tồn (Survivor) và bắn súng tự động (Auto-Shooter) trong môi trường 2D, tập trung vào khả năng mở rộng hệ thống vũ khí và quản lý kẻ địch theo đợt.

---

## 📖 Giới thiệu

**Shooter2D** là một dự án Unity hoàn chỉnh, triển khai các cơ chế cốt lõi của dòng game sinh tồn hiện đại (như Vampire Survivors). Dự án tập trung vào việc tối ưu hóa hiệu suất khi xử lý số lượng lớn kẻ địch và hệ thống nâng cấp nhân vật năng động.

### Các trụ cột cốt lõi:
*   **Hệ thống chiến đấu tự động (Auto-Combat):** Cơ chế tự động tìm mục tiêu và khai hỏa thông minh.
*   **Quản lý tài nguyên & Tiến trình:** Hệ thống Kinh nghiệm (XP), Cấp độ (Level) và các bảng nâng cấp.
*   **Trí tuệ nhân tạo (Advanced AI):** Tích hợp A* Pathfinding để kẻ địch di chuyển thông minh hơn.

---

## ✨ Các Tính Năng Nổi Bật

### ⚔️ Hệ Thống Chiến Đấu (Combat System)
*   **Auto-Targeting:** Vũ khí tự động xác định và xoay về phía kẻ địch gần nhất.
*   **Multi-Weapon Management:** Quản lý đồng thời nhiều loại vũ khí với các chỉ số riêng biệt (sát thương, tốc độ bắn, tầm bắn).
*   **Projectile Logic:** Hệ thống đạn đạo có hiệu ứng Muzzle, va chạm và gây sát thương ngẫu nhiên trong khoảng (min/max damage).
*   **Special Effects:** Cơ chế đóng băng kẻ địch (Freeze) và các hiệu ứng SFX đi kèm.

### 🌊 Quản Lý Kẻ Địch & Spawn (Enemy & Spawner)
*   **Wave System:** `SpawnerManager` điều phối các đợt tấn công của kẻ địch theo thời gian.
*   **Pathfinding:** Kẻ địch sử dụng `Seeker` và `Path` để vượt qua vật cản, đuổi theo người chơi một cách tối ưu.
*   **Scaling Difficulty:** Chỉ số của kẻ địch có thể điều chỉnh linh hoạt theo tiến trình trò chơi.

### 📈 Tiến Trình & UI (Progression & Interface)
*   **XP & Leveling:** Hệ thống thu thập kinh nghiệm và thăng cấp nhân vật.
*   **UI Dynamic:** Thanh máu (HealthBar) động, bảng nâng cấp (LevelUpPanel) và bảng kết thúc (LosePanel).
*   **Timer System:** Đồng hồ đếm ngược/tiến để quản lý thời gian sinh tồn.

---

## 🛠️ Công Nghệ Sử Dụng

| Thành phần | Công nghệ | Chi tiết |
| :--- | :--- | :--- |
| **Engine** | Unity 2022.3.x | Long Term Support (LTS) |
| **Navigation** | A* Pathfinding Project | Xử lý đường đi phức tạp cho AI |
| **Scripting** | C# (Object Oriented) | Sử dụng Manager Pattern & Singleton |
| **Physics** | Physics 2D | Xử lý va chạm và lực đẩy đạn đạo |
| **UI** | Unity UI (uGUI) | Hệ thống Canvas linh hoạt |
| **Audio** | Audio Source/Clip | Quản lý hiệu ứng âm thanh (SFX) |

---

## 📁 Cấu Trúc Thư Mục

```text
Assets/
├── Animation/        # Clips cho nhân vật, kẻ địch và hiệu ứng
├── Audio/            # Tài nguyên âm thanh (SFX & Music)
├── Prefabs/          # Các đối tượng quan trọng (Bullet, Enemy, Player, UI)
├── Resources/        # Tài nguyên tải động trong runtime
├── Scenes/           # Các màn chơi và giao diện chính
├── Scripts/          # Toàn bộ logic điều khiển dự án
│   ├── Effect/       # Xử lý hiệu ứng hình ảnh/âm thanh
│   ├── UI/           # Quản lý các Panel và giao diện
│   ├── Weapon/       # Logic vũ khí và đạn đạo
│   └── Enemy/        # AI và hệ thống Spawner
├── Sprites/          # Hình ảnh Pixel Art / 2D Assets
└── Tileset/          # Dữ liệu xây dựng môi trường (Map)
```

---

## 🚀 Hướng Dẫn Khởi Chạy

1. **Yêu cầu:** Unity 2022.3.x trở lên.
2. **Cài đặt:**
   * Clone repository hoặc tải source code.
   * Mở dự án bằng Unity Hub.
   * Đảm bảo plugin **A* Pathfinding Project** được cấu hình đúng trong phần `Plugins`.
3. **Chạy Game:**
   * Mở Scene chính tại `Assets/Scenes/Main.unity`.
   * Nhấn nút **Play**.

---

## 🎯 Lộ Trình Phát Triển (Roadmap)

- [x] Hệ thống di chuyển và tự động bắn.
- [x] Hệ thống XP, thăng cấp và chọn nâng cấp.
- [x] AI tìm đường cơ bản với A*.
- [ ] Thêm đa dạng loại kẻ địch (Boss, Kẻ địch tầm xa).
- [ ] Triển khai hệ thống Shop/Vật phẩm trang bị lâu dài.
- [ ] Tối ưu hóa Object Pooling cho đạn và kẻ địch để cải thiện FPS.
- [ ] Hệ thống lưu trữ thành tích (Highscore).

---

## 👨‍💻 Tác Giả

**Tunaanhgamedev**
* GitHub: [@Tunaanhgamedev](https://github.com/Tunaanhgamedev)
* Facebook: [Tuna Anh](https://www.facebook.com/tuna.anh.225285/)

---

## 📜 Giấy Phép (License)

Dự án được bảo hộ bởi giấy phép **MIT**. Mọi đóng góp đều được chào đón!

---

⭐ **Ủng hộ:** Nếu dự án này giúp ích cho bạn, hãy nhấn **Star** để khích lệ tác giả nhé!
