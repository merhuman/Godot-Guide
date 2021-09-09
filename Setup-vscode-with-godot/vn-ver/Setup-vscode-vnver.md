# Hướng dẫn setup vscode với Godot engine
## Yêu cầu:
### Godot engine
Bạn có thể tải trực tiếp Godot engine tại theo đường dẫn sau:
https://godotengine.org/download

Hoặc tải từ Steam store (nếu như có steam account).

Lưu ý: Bản Godot tải từ Steam store chỉ hỗ trợ GDScript. Còn bản tải trực tiếp từ url trên thì bạn có thể tuỳ chọn bản hỗ trợ C# hoặc bản mặc định GDScript.

### Visual Studio code
Sau khi tải vscode, bạn search Godot trong Extentions.
Chọn godot-tools và install.

## Setup
1. Godot:
Trong project của bạn, chọn Editor/Editor Settings/Text Editor/External.
Trong phần bên phải cửa sổ bạn chỉnh như sau:
- Tick vào Use External Editor.
- Exec Path: <path của vs code>
- Exec Flags: {project} --goto {file}:{line}:{col}

2. Vscode:
Sau khi install extension godot-tools, bạn mở Extention Settings ra và làm như sau:
- Editor Path: <path của godot.exe>
- Gdscript-lsp-server-port: 6008
- Gdscript-lsp-protool: tcp cho bản Godot 3.2.2 trở lên, ngược lại chọn ws.
- Check status: có thể để trống.

3. Cài đặt VSIX file:
- Down file VSIX từ đường dẫn sau.
https://github.com/godotengine/godot-vscode-plugin/files/4810957/godot-tools-eventfix.zip
- Giải nén file rồi copy vào thư mục project godot của bạn.
- Mở folder project đó lên bằng vscode.
- Click vào file VSIX trong cây thư mục để tiến hành cài đặt.

Tới đây thì bạn đã có thể edit code cũng như debug trực tiếp ngay trên vscode rồi đó.