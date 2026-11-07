# Đồ án UTM Firewall với OPNsense

Đồ án An toàn mạng NT140.R11.ANTT nghiên cứu, triển khai và cấu hình hệ thống Unified Threat Management (UTM) Firewall nhằm bảo vệ an ninh mạng.

## Mục tiêu

- Triển khai OPNsense làm cổng bảo mật trong môi trường ảo hóa.
- Kiểm soát lưu lượng giữa mạng WAN và mạng LAN cô lập.
- Khảo sát firewall, NAT, DHCP, DNS, logging, IDS/IPS, VPN và web filtering.
- Xây dựng quy trình kiểm thử lặp lại được và lưu bằng chứng phục vụ đánh giá.

## Mô hình phòng lab dự kiến

| Hệ thống | Vai trò | Cấu hình tối thiểu |
|---|---|---|
| OPNsense | UTM firewall và default gateway | 2 vCPU, 3–4 GB RAM, 2 network adapter |
| Ubuntu | Máy khách kiểm thử trong LAN | 2 vCPU, 2 GB RAM |
| Windows | Máy khách kiểm thử trong LAN | 2 vCPU, 4 GB RAM |

WAN của OPNsense kết nối VMware NAT và nhận địa chỉ qua DHCP. LAN kết nối mạng ảo cô lập, sử dụng gateway `192.168.10.1/24`.

## Tài liệu theo tuần

- [Tuần 2: Thiết kế mạng và kế hoạch kiểm thử chính sách firewall](docs/week-2-network-design.md)
- [Tuần 4: Runbook triển khai nền tảng OPNsense trên VMware](docs/week-4-opnsense-baseline.md)

## Trạng thái

Tuần 2 đã hoàn thành thiết kế topology, kế hoạch địa chỉ, luồng lưu lượng và kết quả kỳ vọng của các chính sách firewall. Tuần 4 bổ sung runbook triển khai, baseline DHCP/DNS/NAT/firewall và ma trận nghiệm thu. Kết quả thực tế, log và ảnh minh chứng chỉ được cập nhật sau khi chạy trên môi trường lab.
