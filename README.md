# ConnectSphere - 点对点文件传输 Web 应用 
**ConnectSphere（灵犀传）** 是一款简洁、直观的基于 **PeerJS** 和 **WebRTC** 技术的点对点（P2P）文件传输 Web 应用。它允许用户在设备间直接传输文件，无需依赖中央服务器，确保快速且安全的传输。应用采用现代暗色主题界面，支持二维码分享和实时进度跟踪，让文件分享变得简单高效。

**ConnectSphere** is a sleek and intuitive web application for peer-to-peer (P2P) file transfer, built with **PeerJS** and **WebRTC**. It enables users to share files directly between devices without a central server, ensuring fast and secure transfers. With a modern dark-themed interface, QR code support, and real-time progress tracking, ConnectSphere makes file sharing simple and efficient.

## 功能 / Features
- **分享模式 / Share Mode**: 选择文件，生成分享链接或二维码，等待接收者连接。  
  Select a file, generate a shareable link or QR code, and wait for receivers to connect.
- **接收模式 / Receive Mode**: 粘贴分享链接，连接并下载文件。  
  Paste a share link to connect and download files.
- **拖放支持 / Drag-and-Drop**: 通过拖放或点击选择文件，操作简便。  
  Easily upload files via drag-and-drop or file selection.
- **实时反馈 / Real-Time Feedback**: 监控传输进度、速度和连接状态。  
  Monitor transfer progress, speed, and connection status.
- **多接收者支持 / Multi-Receiver Support**: 同时与多个接收者分享文件。  
  Share files with multiple receivers simultaneously.
- **错误处理 / Error Handling**: 强大的重试机制和友好的错误通知。  
  Robust retry mechanism and user-friendly error notifications.
- **响应式设计 / Responsive Design**: 适配桌面和移动设备。  
  Optimized for both desktop and mobile devices.

## 技术栈 / Tech Stack
- **HTML5 & CSS3**: 现代、响应式用户界面，采用暗色主题和渐变效果。  
  Modern, responsive UI with a dark theme and gradient effects.
- **JavaScript**: 文件处理和 P2P 通信的核心逻辑。  
  Core logic for file handling and P2P communication.
- **PeerJS**: 简化 WebRTC 的实现，用于建立 P2P 连接。  
  Simplifies WebRTC for establishing P2P connections.
- **QRCode.js**: 生成二维码，便于移动端分享。  
  Generates QR codes for easy mobile sharing.
- **WebRTC**: 通过 STUN 服务器实现无服务器文件传输。  
  Enables direct, serverless file transfers via STUN servers.
- **FileReader API**: 支持分片读取文件，优化大文件传输。  
  Supports chunked file reading for efficient large file transfers.

## 快速开始 / Getting Started

### 前置条件 / Prerequisites
- 现代浏览器（例如 Chrome、Firefox、Safari），支持 WebRTC。  
  A modern web browser (e.g., Chrome, Firefox, Safari) with WebRTC support.
- 无需服务器配置，应用完全在浏览器中运行。  
  No server setup required; the app runs entirely in the browser.

### 安装 / Installation
1. 克隆仓库：  
   Clone the repository:
   ```bash
   git clone https://github.com/your-username/connectsphere.git
   ```
2. 在浏览器中打开 `index.html`，或通过本地服务器（如 VS Code 的 Live Server）托管。  
   Open `index.html` in a web browser, or host it on a local server (e.g., using `Live Server` in VS Code).

### 使用方法 / Usage
1. **分享文件 / Share Files**:
   - 选择“分享”模式。  
     Select "Share" mode.
   - 拖放文件或点击选择文件。  
     Drag and drop a file or click to select one.
   - 生成分享链接或二维码。  
     Generate a share link or QR code.
   - 将链接/二维码分享给接收者。  
     Share the link/QR code with the receiver.
   - 监控已连接的接收者和传输进度。  
     Monitor connected receivers and transfer progress.

2. **接收文件 / Receive Files**:
   - 选择“接收”模式。  
     Select "Receive" mode.
   - 粘贴分享者提供的分享链接。  
     Paste the share link provided by the sharer.
   - 连接并开始下载文件。  
     Connect and start downloading the file.
   - 实时跟踪下载进度和速度。  
     Track download progress and speed in real time.

3. **二维码 / QR Code**:
   - 在分享模式下，点击二维码按钮生成可扫描的二维码，方便移动设备使用。  
     In Share mode, click the QR code button to generate a scannable code for mobile devices.

## 工作原理 / How It Works
- **PeerJS & WebRTC**: ConnectSphere 使用 PeerJS 管理 WebRTC 连接，配置多个信令服务器以提高可靠性。  
  ConnectSphere uses PeerJS to manage WebRTC connections, with multiple signaling servers for reliability.
- **文件分片 / File Chunking**: 大文件被分割成 256KB 的分片，优化传输效率并减少内存占用。  
  Large files are split into 256KB chunks to optimize transfer and reduce memory usage.
- **错误处理 / Error Handling**: 自动重试（最多 3 次）和备用信令服务器确保连接稳定。  
  Automatic retries (up to 3 attempts) and fallback signaling servers ensure robust connections.
- **用户界面反馈 / UI Feedback**: 进度条、速度指示器和动画通知让用户随时了解状态。  
  Progress bars, speed indicators, and animated notifications keep users informed.

## 限制 / Limitations
- 在受限网络（例如严格防火墙）中，WebRTC 可能无法正常工作。  
  WebRTC may not work in restricted networks (e.g., behind strict firewalls).
- 大文件传输依赖浏览器内存和网络稳定性。  
  Large file transfers depend on browser memory and network stability.
- 暂无端到端加密（计划在未来更新中添加）。  
  No end-to-end encryption (planned for future updates).

## 未来改进 / Future Improvements
- 添加端到端加密以增强安全性。  
  Add end-to-end encryption for enhanced security.
- 支持一次性上传多个文件。  
  Support multiple file uploads in a single session.
- 实现断点续传功能，允许中断后恢复传输。  
  Implement resume functionality for interrupted transfers.
- 允许用户设置自定义 Peer ID，简化连接。  
  Allow custom Peer IDs for easier connection.
- 在接收端支持图片和视频的预览功能。  
  Add file preview for images and videos on the receiver side.

## 贡献 / Contributing
欢迎贡献代码！请按照以下步骤操作：  
Contributions are welcome! Please follow these steps:
1. Fork 仓库。  
   Fork the repository.
2. 创建新分支（`git checkout -b feature/your-feature`）。  
   Create a new branch (`git checkout -b feature/your-feature`).
3. 提交更改（`git commit -m 'Add your feature'`）。  
   Commit your changes (`git commit -m 'Add your feature'`).
4. 推送分支（`git push origin feature/your-feature`）。  
   Push to the branch (`git push origin feature/your-feature`).
5. 提交 Pull Request。  
   Open a Pull Request.

## 许可证 / License
本项目采用 MIT 许可证，详情见 [LICENSE](LICENSE) 文件。  
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 致谢 / Acknowledgments
- [PeerJS](https://peerjs.com/)，简化了 WebRTC 的实现。  
  [PeerJS](https://peerjs.com/) for simplifying WebRTC.
- [QRCode.js](https://davidshimjs.github.io/qrcodejs/)，用于生成二维码。  
  [QRCode.js](https://davidshimjs.github.io/qrcodejs/) for QR code generation.
