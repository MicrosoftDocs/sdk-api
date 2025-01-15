---
UID: NF:dbghelp.StackWalk2
title: StackWalk2 function (dbghelp.h)
description: Obtains a stack trace. (StackWalk2)
helpviewer_keywords: ["IMAGE_FILE_MACHINE_AMD64","IMAGE_FILE_MACHINE_I386","IMAGE_FILE_MACHINE_IA64","IMAGE_FILE_MACHINE_ARM64","SYM_STKWALK_DEFAULT","SYM_STKWALK_FORCE_FRAMEPTR","StackWalk2","StackWalk2 function","dbghelp/StackWalk2"]
tech.root: Debug
ms.assetid: D0ED2879-CABE-47ff-AB0E-9B50943033A4
ms.date: 1/13/2025
ms.keywords: IMAGE_FILE_MACHINE_AMD64, IMAGE_FILE_MACHINE_I386, IMAGE_FILE_MACHINE_IA64, IMAGE_FILE_MACHINE_ARM64, SYM_STKWALK_DEFAULT, SYM_STKWALK_FORCE_FRAMEPTR, StackWalk2, StackWalk2 function, dbghelp/StackWalk2
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 10.0.22621.4602 or later
ms.custom: 22H2
f1_keywords:
 - StackWalk2
 - dbghelp/StackWalk2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - StackWalk2
---

# StackWalk2 function


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
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_ARM64"></a><a id="image_file_machine_arm64"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_ARM64</b></dt>
<dt>0xaa64</dt>
</dl>
</td>
<td width="60%">
ARM64

</td>
</tr>
</table>

### -param hProcess [in]

A handle to the process for which the stack trace is generated. If the caller supplies a valid callback 
      pointer for the <i>ReadMemoryRoutine</i> parameter, then this value does not have to be a 
      valid process handle. It can be a token that is unique and consistently the same for all calls to the 
      <b>StackWalk2</b> function. If the symbol handler is used with 
      <b>StackWalk2</b>, use the same process handles for the calls 
      to each function.

### -param hThread [in]

A handle to the thread for which the stack trace is generated. If the caller supplies a valid callback 
      pointer for the <i>ReadMemoryRoutine</i> parameter, then this value does not have to be a 
      valid thread handle. It can be a token that is unique and consistently the same for all calls to the 
      <b>StackWalk2</b> function.

### -param StackFrame [in, out]

A pointer to a <a href="/windows/desktop/api/dbghelp/ns-dbghelp-stackframe_ex">STACKFRAME_EX</a> structure. This 
      structure receives information for the next frame, if the function call succeeds.

### -param ContextRecord [in, out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure. This parameter is 
       required only when the <i>MachineType</i> parameter is not 
       <b>IMAGE_FILE_MACHINE_I386</b>. However, it is recommended that this parameter contain a 
       valid context record. This allows <b>StackWalk2</b> to handle 
       a greater variety of situations.

This context may be modified, so do not pass a context record that should not be modified.

### -param ReadMemoryRoutine [in, optional]

A callback routine that provides memory read services. When the 
       <b>StackWalk2</b> function needs to read memory from the 
       process's address space, the 
       <a href="/windows/desktop/api/dbghelp/nc-dbghelp-pread_process_memory_routine">ReadProcessMemoryProc64</a> callback is 
       used.

If this parameter is <b>NULL</b>, then the function uses a default routine. In this case, 
       the <i>hProcess</i> parameter must be a valid process handle.

If this parameter is not 
       <b>NULL</b>, the application should implement and register a symbol handler callback 
       function that handles <b>CBA_READ_MEMORY</b>.

### -param FunctionTableAccessRoutine [in, optional]

A callback routine that provides access to the run-time function table for the process. This parameter is 
       required because the <b>StackWalk2</b> function does not have 
       access to the process's run-time function table. For more information, see 
       <a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfunction_table_access_routine">FunctionTableAccessProc64</a>.

The symbol handler provides functions that load and access the run-time table. If these functions are used, 
       then <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfunctiontableaccess">SymFunctionTableAccess64</a> can be 
       passed as a valid parameter.

### -param GetModuleBaseRoutine [in, optional]

A callback routine that provides a module base for any given virtual address. This parameter is required. 
       For more information, see 
       <a href="/windows/desktop/api/dbghelp/nc-dbghelp-pget_module_base_routine">GetModuleBaseProc64</a>.

The symbol handler provides functions that load and maintain module information. If these functions are used, 
       then <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetmodulebase">SymGetModuleBase64</a> can be passed as a valid 
       parameter.

### -param TranslateAddress [in, optional]

A callback routine that provides address translation for 16-bit addresses. For more information, see 
       <a href="/windows/desktop/api/dbghelp/nc-dbghelp-ptranslate_address_routine">TranslateAddressProc64</a>.

Most callers of <b>StackWalk2</b> can safely pass 
       <b>NULL</b> for this parameter.

### -param GetTargetAttributeValue [in, optional]

A callback routine that provides the values of target attributes required to walk the stack.  For more information, see
        <a href="/windows/desktop/api/dbghelp/nc-dbghelp-get_target_attribute_value_routine">GetTargetAttributeValue</a>.

Many callers of <b>StackWalk2</b> can safely pass
        <b>NULL</b> for this parameter.  Callers on ARM64 platforms which may utilize pointer authentication should provide a callback.

### -param Flags [in]

A combination of zero or more flags.



#### SYM_STKWALK_DEFAULT (0)



#### SYM_STKWALK_FORCE_FRAMEPTR (1)

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. Note that 
       <b>StackWalk2</b> generally does not set the last error 
       code.

## -remarks

The <b>StackWalk2</b> function provides a portable method 
    for obtaining a stack trace. Using the <b>StackWalk2</b> 
    function is recommended over writing your own function because of all the complexities associated with stack 
    walking on platforms. In addition, there are compiler options that cause the stack to appear differently, 
    depending on how the module is compiled. By using this function, your application has a portable stack trace that 
    continues to work as the compiler and operating system change.

The first call to this function will fail if the <b>AddrPC</b>,  
    <b>AddrFrame</b>, and <b>AddrStack</b> members of the 
    <a href="/windows/desktop/api/dbghelp/ns-dbghelp-stackframe">STACKFRAME64</a> structure passed in the 
    <i>StackFrame</i> parameter are not initialized.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfunction_table_access_routine">FunctionTableAccessProc64</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pread_process_memory_routine">ReadProcessMemoryProc64</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-stackframe_ex">STACKFRAME_EX</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfunctiontableaccess">SymFunctionTableAccess64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetmodulebase">SymGetModuleBase64</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-ptranslate_address_routine">TranslateAddressProc64</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pget_target_attribute_value_routine">GetTargetAttributeValueProc64</a>