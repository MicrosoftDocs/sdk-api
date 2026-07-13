---
UID: NF:dbghelp.StackWalk2
title: StackWalk2 function (dbghelp.h)
description: Obtains a stack trace. (StackWalk2)
helpviewer_keywords: ["IMAGE_FILE_MACHINE_AMD64","IMAGE_FILE_MACHINE_I386","IMAGE_FILE_MACHINE_IA64","IMAGE_FILE_MACHINE_ARM64","SYM_STKWALK_DEFAULT","SYM_STKWALK_FORCE_FRAMEPTR","StackWalk2","StackWalk2 function","dbghelp/StackWalk2"]
tech.root: Debug
ms.assetid: D0ED2879-CABE-47ff-AB0E-9B50943033A4
ms.date: 01/23/2025
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

The architecture type of the computer for which the stack trace is generated. This parameter can be one of the following values.

| Value                      | Meaning          |
|----------------------------|------------------|
| **IMAGE_FILE_MACHINE_I386**<br>0x014c           | Intel x86        |
| **IMAGE_FILE_MACHINE_IA64**<br>0x0200           | Intel Itanium    |
| **IMAGE_FILE_MACHINE_AMD64**<br>0x8664          | x64 (AMD64 or EM64T) |
| **IMAGE_FILE_MACHINE_ARM64**<br>0xaa64          | ARM64            |

### -param hProcess [in]

A handle to the process for which the stack trace is generated. If the caller supplies a valid callback pointer for the *ReadMemoryRoutine* parameter, then this value does not have to be a valid process handle. It can be a token that is unique and consistently the same for all calls to the **StackWalk2** function. If the symbol handler is used with **StackWalk2**, use the same process handles for the calls to each function.

### -param hThread [in]

A handle to the thread for which the stack trace is generated. If the caller supplies a valid callback pointer for the *ReadMemoryRoutine* parameter, then this value does not have to be a valid thread handle. It can be a token that is unique and consistently the same for all calls to the **StackWalk2** function.

### -param StackFrame [in, out]

A pointer to a [STACKFRAME_EX structure](ns-dbghelp-stackframe_ex.md). This structure receives information for the next frame, if the function call succeeds.

### -param ContextRecord [in, out]

A pointer to an [ARM64_NT_CONTEXT structure](../winnt/ns-winnt-arm64_nt_context.md). This parameter is required only when the *MachineType* parameter is not **IMAGE_FILE_MACHINE_I386**. However, it is recommended that this parameter contain a valid context record. This allows **StackWalk2** to handle a greater variety of situations.

This context may be modified, so do not pass a context record that should not be modified.

### -param ReadMemoryRoutine [in, optional]

A callback routine that provides memory read services. When the **StackWalk2** function needs to read memory from the process's address space, the [ReadProcessMemoryProc64 callback function](nc-dbghelp-pread_process_memory_routine64.md) is used.

If this parameter is **NULL**, then the function uses a default routine. In this case, the *hProcess* parameter must be a valid process handle.

If this parameter is not **NULL**, the application should implement and register a symbol handler callback function that handles **CBA_READ_MEMORY**.

### -param FunctionTableAccessRoutine [in, optional]

A callback routine that provides access to the run-time function table for the process. This parameter is required because the **StackWalk2** function does not have access to the process's run-time function table. For more information, see [FunctionTableAccessProc64 callback function](nc-dbghelp-pfunction_table_access_routine64.md).

The symbol handler provides functions that load and access the run-time table. If these functions are used, then the [SymFunctionTableAccess64 function](nf-dbghelp-symfunctiontableaccess64.md) can be passed as a valid parameter.

### -param GetModuleBaseRoutine [in, optional]

A callback routine that provides a module base for any given virtual address. This parameter is required. For more information, see [PGET_MODULE_BASE_ROUTINE64 callback function](nc-dbghelp-pget_module_base_routine64.md).

The symbol handler provides functions that load and maintain module information. If these functions are used, then the [SymGetModuleBase64 function](nf-dbghelp-symgetmodulebase64.md) can be passed as a valid parameter.

### -param TranslateAddress [in, optional]

A callback routine that provides address translation for 16-bit addresses. For more information, see [PTRANSLATE_ADDRESS_ROUTINE64 callback function](nc-dbghelp-ptranslate_address_routine64.md).

Most callers of **StackWalk2** can safely pass **NULL** for this parameter.

### -param GetTargetAttributeValue [in, optional]

A callback routine that provides the values of target attributes required to walk the stack.  For more information, see [PGET_TARGET_ATTRIBUTE_VALUE64 callback function](nc-dbghelp-pget_target_attribute_value64.md).

Many callers of **StackWalk2** can safely pass **NULL** for this parameter.  Callers on ARM64 platforms which may utilize pointer authentication should provide a callback.

### -param Flags [in]

A combination of zero or more flags.

#### SYM_STKWALK_DEFAULT (0)

#### SYM_STKWALK_FORCE_FRAMEPTR (1)

## -returns

If the function succeeds, the return value is **TRUE**.

If the function fails, the return value is **FALSE**. Note that **StackWalk2** generally does not set the last error code.

## -remarks

The **StackWalk2** function provides a portable method for obtaining a stack trace. Using the **StackWalk2** function is recommended over writing your own function because of all the complexities associated with stack walking on platforms. In addition, there are compiler options that cause the stack to appear differently, depending on how the module is compiled. By using this function, your application has a portable stack trace that continues to work as the compiler and operating system change.

The first call to this function will fail if the **AddrPC**,  **AddrFrame**, and **AddrStack** members of the [STACKFRAME64 structure](ns-dbghelp-stackframe64.md) passed in the *StackFrame* parameter are not initialized.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

[ARM64_NT_CONTEXT structure](../winnt/ns-winnt-arm64_nt_context.md)

[DbgHelp Functions](/windows/desktop/Debug/dbghelp-functions)

[FunctionTableAccessProc64 callback function](nc-dbghelp-pfunction_table_access_routine64.md)

[ReadProcessMemoryProc64 callback function](nc-dbghelp-pread_process_memory_routine64.md)

[STACKFRAME_EX structure](ns-dbghelp-stackframe_ex.md)

[SymFunctionTableAccess64 function](nf-dbghelp-symfunctiontableaccess64.md)

[SymGetModuleBase64 function](nf-dbghelp-symgetmodulebase64.md)

[PTRANSLATE_ADDRESS_ROUTINE64 callback function](nc-dbghelp-ptranslate_address_routine64.md)

[PGET_TARGET_ATTRIBUTE_VALUE64 callback function](nc-dbghelp-pget_target_attribute_value64.md)
