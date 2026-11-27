# buildlldb-dap

Builds a native 32-bit Windows `lldb-dap.exe` from LLVM 18.1.8 for debugging
`win32` programs from a 64-bit tkEdit host.

Run the **build-i686-lldb-dap** GitHub Actions workflow manually. Each successful
run publishes:

- an Actions artifact named `lldb-dap-i686`;
- a reusable GitHub Release tagged `lldb-dap-i686-llvm18.1.8`, containing
  `lldb-dap.exe`, its LLDB/LLVM runtime DLLs, and the x86 Visual C++ runtime
  DLLs needed on machines without that redistributable installed.

In tkEdit, set `[debug] adapter` to the downloaded executable, or set
`TKEDIT_LLDB_DAP` to its full path for a test or portable toolchain.
