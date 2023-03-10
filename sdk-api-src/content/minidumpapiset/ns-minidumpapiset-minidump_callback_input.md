---
UID: NS:minidumpapiset._MINIDUMP_CALLBACK_INPUT
title: MINIDUMP_CALLBACK_INPUT (minidumpapiset.h)
description: Contains information used by the MiniDumpCallback function.
helpviewer_keywords: ["*PMINIDUMP_CALLBACK_INPUT","MINIDUMP_CALLBACK_INPUT","MINIDUMP_CALLBACK_INPUT structure","PMINIDUMP_CALLBACK_INPUT","PMINIDUMP_CALLBACK_INPUT structure pointer","_MINIDUMP_CALLBACK_INPUT","_win32_minidump_callback_input_str","base.minidump_callback_input_str","minidumpapiset/MINIDUMP_CALLBACK_INPUT","minidumpapiset/PMINIDUMP_CALLBACK_INPUT"]
old-location: base\minidump_callback_input_str.htm
tech.root: Debug
ms.assetid: 0ce3083c-21c9-48a4-9099-1dab31afcafa
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_CALLBACK_INPUT, MINIDUMP_CALLBACK_INPUT, MINIDUMP_CALLBACK_INPUT structure, PMINIDUMP_CALLBACK_INPUT, PMINIDUMP_CALLBACK_INPUT structure pointer, _MINIDUMP_CALLBACK_INPUT, _win32_minidump_callback_input_str, base.minidump_callback_input_str, minidumpapiset/MINIDUMP_CALLBACK_INPUT, minidumpapiset/PMINIDUMP_CALLBACK_INPUT'
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MINIDUMP_CALLBACK_INPUT, *PMINIDUMP_CALLBACK_INPUT
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_CALLBACK_INPUT
 - minidumpapiset/_MINIDUMP_CALLBACK_INPUT
 - PMINIDUMP_CALLBACK_INPUT
 - minidumpapiset/PMINIDUMP_CALLBACK_INPUT
 - MINIDUMP_CALLBACK_INPUT
 - minidumpapiset/MINIDUMP_CALLBACK_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_CALLBACK_INPUT
---

# MINIDUMP_CALLBACK_INPUT structure


## -description

Contains information used by the 
<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function.

## -struct-fields

### -field ProcessId

The identifier of the process that contains callback function.

This member is not used if <b>CallbackType</b> is <b>IoStartCallback</b>.

### -field ProcessHandle

A handle to the process that contains the callback function.

This member is not used if <b>CallbackType</b> is <b>IoStartCallback</b>.

### -field CallbackType

The type of callback function. This member can be one of the values in the 
<a href="/windows/win32/api/minidumpapiset/ne-minidumpapiset-minidump_callback_type">MINIDUMP_CALLBACK_TYPE</a> enumeration.

### -field Status

If <b>CallbackType</b> is <b>KernelMinidumpStatusCallback</b>, the union is an <b>HRESULT</b> value that indicates the status of the kernel minidump write attempt.

### -field Thread

If <b>CallbackType</b> is <b>ThreadCallback</b>, the union is a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_callback">MINIDUMP_THREAD_CALLBACK</a> structure.

### -field ThreadEx

If <b>CallbackType</b> is <b>ThreadExCallback</b>, the union is a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_ex_callback">MINIDUMP_THREAD_EX_CALLBACK</a> structure.

### -field Module

If <b>CallbackType</b> is <b>ModuleCallback</b>, the union is a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_module_callback">MINIDUMP_MODULE_CALLBACK</a> structure.

### -field IncludeThread

If <b>CallbackType</b> is <b>IncludeThreadCallback</b>, the union is a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_include_thread_callback">MINIDUMP_INCLUDE_THREAD_CALLBACK</a> structure.

<b>DbgHelp 6.2 and earlier:  </b>This member is not available.

### -field IncludeModule

If <b>CallbackType</b> is <b>IncludeModuleCallback</b>, the union is a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_include_module_callback">MINIDUMP_INCLUDE_MODULE_CALLBACK</a> structure.

<b>DbgHelp 6.2 and earlier:  </b>This member is not available.

### -field Io

If <b>CallbackType</b> is <b>IoStartCallback</b>, <b>IoWriteAllCallback</b>, or <b>IoFinishCallback</b>, the union is a <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_io_callback">MINIDUMP_IO_CALLBACK</a> structure.

<b>DbgHelp 6.4 and earlier:  </b>This member is not available.

### -field ReadMemoryFailure

If <b>CallbackType</b> is <b>ReadMemoryFailureCallback</b>, the union is a <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_read_memory_failure_callback">MINIDUMP_READ_MEMORY_FAILURE_CALLBACK</a> structure.

<b>DbgHelp 6.4 and earlier:  </b>This member is not available.

### -field SecondaryFlags

Contains a value from the <a href="/windows/win32/api/minidumpapiset/ne-minidumpapiset-minidump_secondary_flags">MINIDUMP_SECONDARY_FLAGS</a> enumeration type.

<b>DbgHelp 6.5 and earlier:  </b>This member is not available.

### -field VmQuery

### -field VmPreRead

### -field VmPostRead

## -remarks

If <b>CallbackType</b> is <b>CancelCallback</b> or <b>MemoryCallback</b>, the <b>ProcessId</b>, <b>ProcessHandle</b>, and <b>CallbackType</b> members are valid but no other input is specified.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ne-minidumpapiset-minidump_callback_type">MINIDUMP_CALLBACK_TYPE</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_include_module_callback">MINIDUMP_INCLUDE_MODULE_CALLBACK</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_include_thread_callback">MINIDUMP_INCLUDE_THREAD_CALLBACK</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_io_callback">MINIDUMP_IO_CALLBACK</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_module_callback">MINIDUMP_MODULE_CALLBACK</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_read_memory_failure_callback">MINIDUMP_READ_MEMORY_FAILURE_CALLBACK</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_callback">MINIDUMP_THREAD_CALLBACK</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_ex_callback">MINIDUMP_THREAD_EX_CALLBACK</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>