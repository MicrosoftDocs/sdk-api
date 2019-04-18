---
UID: NF:dbghelp.StackWalk64
title: StackWalk64 function (dbghelp.h)
author: windows-sdk-content
description: Obtains a stack trace.
old-location: base\stackwalk64.htm
tech.root: Debug
ms.assetid: e2bdaa4c-5474-41a0-bcea-927570c8402c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMAGE_FILE_MACHINE_AMD64, IMAGE_FILE_MACHINE_I386, IMAGE_FILE_MACHINE_IA64, StackWalk, StackWalk function, StackWalk64, StackWalk64 function, _win32_stackwalk64, base.stackwalk64, dbghelp/StackWalk, dbghelp/StackWalk64
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - StackWalk64
 - StackWalk
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# StackWalk64 function


## -description


Obtains a stack trace.


## -parameters




### -param MachineType [in]

The architecture type of the computer for which the stack trace is generated. This parameter can be one of 
      the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_I386"></a><a id="image_file_machine_i386"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_I386</b></dt>
<dt>0x014c</dt>
</dl>
</td>
<td width="60%">
Intel x86

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_IA64"></a><a id="image_file_machine_ia64"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_IA64</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Intel Itanium

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_AMD64"></a><a id="image_file_machine_amd64"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_AMD64</b></dt>
<dt>0x8664</dt>
</dl>
</td>
<td width="60%">
x64 (AMD64 or EM64T)

</td>
</tr>
</table>
 


### -param hProcess [in]

A handle to the process for which the stack trace is generated. If the caller supplies a valid callback 
      pointer for the <i>ReadMemoryRoutine</i> parameter, then this value does not have to be a 
      valid process handle. It can be a token that is unique and consistently the same for all calls to the 
      <b>StackWalk64</b> function. If the symbol handler is used with 
      <b>StackWalk64</b>, use the same process handles for the calls 
      to each function.


### -param hThread [in]

A handle to the thread for which the stack trace is generated. If the caller supplies a valid callback 
     pointer for the <i>ReadMemoryRoutine</i> parameter, then this value does not have to be a 
     valid thread handle. It can be a token that is unique and consistently the same for all calls to the 
     <b>StackWalk64</b> function.


### -param StackFrame [in, out]

A pointer to a <a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a> structure. This 
      structure receives information for the next frame, if the function call succeeds.


### -param ContextRecord [in, out]

A pointer to a <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure. This parameter is 
       required only when the <i>MachineType</i> parameter is not 
       <b>IMAGE_FILE_MACHINE_I386</b>. However, it is recommended that this parameter contain a 
       valid context record. This allows <b>StackWalk64</b> to handle 
       a greater variety of situations.

This context may be modified, so do not pass a context record that should not be modified.


### -param ReadMemoryRoutine [in, optional]

A callback routine that provides memory read services. When the 
       <b>StackWalk64</b> function needs to read memory from the 
       process's address space, the 
       <a href="https://msdn.microsoft.com/84ff0085-295d-48bd-baa5-d6b2845520a6">ReadProcessMemoryProc64</a> callback is 
       used.

If this parameter is <b>NULL</b>, then the function uses a default routine. In this case, 
       the <i>hProcess</i> parameter must be a valid process handle.

If this parameter is not 
       <b>NULL</b>, the application should implement and register a symbol handler callback 
       function that handles <b>CBA_READ_MEMORY</b>.


### -param FunctionTableAccessRoutine [in, optional]

A callback routine that provides access to the run-time function table for the process. This parameter is 
       required because the <b>StackWalk64</b> function does not have 
       access to the process's run-time function table. For more information, see 
       <a href="https://msdn.microsoft.com/387c20b0-ed16-463c-8b11-3ac9a43548a1">FunctionTableAccessProc64</a>.

The symbol handler provides functions that load and access the run-time table. If these functions are used, 
       then <a href="https://msdn.microsoft.com/f79e6af9-9931-4bd7-ae12-29d890267a89">SymFunctionTableAccess64</a> can be 
       passed as a valid parameter.


### -param GetModuleBaseRoutine [in, optional]

A callback routine that provides a module base for any given virtual address. This parameter is required. For 
       more information, see <a href="https://msdn.microsoft.com/a1060d41-183f-4cb1-8214-afef2996ca66">GetModuleBaseProc64</a>.

The symbol handler provides functions that load and maintain module information. If these functions are used, 
       then <a href="https://msdn.microsoft.com/964d0fdb-d982-4509-8c49-0ad0a3491226">SymGetModuleBase64</a> can be passed as a valid 
       parameter.


### -param TranslateAddress [in, optional]

A callback routine that provides address translation for 16-bit addresses. For more information, see 
       <a href="https://msdn.microsoft.com/56c374df-6b48-4649-a914-5cb2f9575bf3">TranslateAddressProc64</a>.

Most callers of <b>StackWalk64</b> can safely pass 
       <b>NULL</b> for this parameter.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. Note that 
       <b>StackWalk64</b> generally does not set the last error 
       code.




## -remarks



The <b>StackWalk64</b> function provides a portable method 
    for obtaining a stack trace. Using the <b>StackWalk64</b> 
    function is recommended over writing your own function because of all the complexities associated with stack 
    walking on platforms. In addition, there are compiler options that cause the stack to appear differently, 
    depending on how the module is compiled. By using this function, your application has a portable stack trace that 
    continues to work as the compiler and operating system change.

The first call to this function will fail if the <b>AddrPC</b>, 
    <b>AddrFrame</b>, and <b>AddrStack</b> members of the 
    <a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a> structure passed in the 
    <i>StackFrame</i> parameter are not initialized.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

This function supersedes the <b>StackWalk</b> function. For 
   more information, see <a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. 
   <b>StackWalk</b> is defined as follows in DbgHelp.h.
   


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define StackWalk StackWalk64
#else
BOOL
IMAGEAPI
StackWalk(
    DWORD MachineType,
    __in HANDLE hProcess,
    __in HANDLE hThread,
    __inout LPSTACKFRAME StackFrame,
    __inout PVOID ContextRecord,
    __in_opt PREAD_PROCESS_MEMORY_ROUTINE ReadMemoryRoutine,
    __in_opt PFUNCTION_TABLE_ACCESS_ROUTINE FunctionTableAccessRoutine,
    __in_opt PGET_MODULE_BASE_ROUTINE GetModuleBaseRoutine,
    __in_opt PTRANSLATE_ADDRESS_ROUTINE TranslateAddress
    );

#endif
```





## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/387c20b0-ed16-463c-8b11-3ac9a43548a1">FunctionTableAccessProc64</a>



<a href="https://msdn.microsoft.com/a1060d41-183f-4cb1-8214-afef2996ca66">GetModuleBaseProc64</a>



<a href="https://msdn.microsoft.com/84ff0085-295d-48bd-baa5-d6b2845520a6">ReadProcessMemoryProc64</a>



<a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a>



<a href="https://msdn.microsoft.com/56c374df-6b48-4649-a914-5cb2f9575bf3">TranslateAddressProc64</a>
 

 

