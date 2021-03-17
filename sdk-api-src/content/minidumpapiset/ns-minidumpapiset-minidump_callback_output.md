---
UID: NS:minidumpapiset._MINIDUMP_CALLBACK_OUTPUT
title: MINIDUMP_CALLBACK_OUTPUT (minidumpapiset.h)
description: Contains information returned by the MiniDumpCallback function.
helpviewer_keywords: ["*PMINIDUMP_CALLBACK_OUTPUT","MINIDUMP_CALLBACK_OUTPUT","MINIDUMP_CALLBACK_OUTPUT structure","PMINIDUMP_CALLBACK_OUTPUT","PMINIDUMP_CALLBACK_OUTPUT structure pointer","_MINIDUMP_CALLBACK_OUTPUT","_win32_minidump_callback_output_str","base.minidump_callback_output_str","minidumpapiset/MINIDUMP_CALLBACK_OUTPUT","minidumpapiset/PMINIDUMP_CALLBACK_OUTPUT"]
old-location: base\minidump_callback_output_str.htm
tech.root: Debug
ms.assetid: 57949087-0f22-40c8-ab56-326a8304c310
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_CALLBACK_OUTPUT, MINIDUMP_CALLBACK_OUTPUT, MINIDUMP_CALLBACK_OUTPUT structure, PMINIDUMP_CALLBACK_OUTPUT, PMINIDUMP_CALLBACK_OUTPUT structure pointer, _MINIDUMP_CALLBACK_OUTPUT, _win32_minidump_callback_output_str, base.minidump_callback_output_str, minidumpapiset/MINIDUMP_CALLBACK_OUTPUT, minidumpapiset/PMINIDUMP_CALLBACK_OUTPUT'
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
req.typenames: MINIDUMP_CALLBACK_OUTPUT, *PMINIDUMP_CALLBACK_OUTPUT
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_CALLBACK_OUTPUT
 - minidumpapiset/_MINIDUMP_CALLBACK_OUTPUT
 - PMINIDUMP_CALLBACK_OUTPUT
 - minidumpapiset/PMINIDUMP_CALLBACK_OUTPUT
 - MINIDUMP_CALLBACK_OUTPUT
 - minidumpapiset/MINIDUMP_CALLBACK_OUTPUT
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
 - MINIDUMP_CALLBACK_OUTPUT
---

# MINIDUMP_CALLBACK_OUTPUT structure


## -description

Contains information returned by the 
<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function.

## -struct-fields

### -field ModuleWriteFlags

The module write operation flags. This member can be one or more of the values in the 
<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-module_write_flags">MODULE_WRITE_FLAGS</a> enumeration. The flags are set to their default values on entry to the callback.

This member is ignored unless the callback type is <b>IncludeModuleCallback</b> or <b>ModuleCallback</b>.

### -field ThreadWriteFlags

The thread write operation flags. This member can be one or more of the values in the 
<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-thread_write_flags">THREAD_WRITE_FLAGS</a> enumeration. The flags are set to their default values on entry to the callback.

This member is ignored unless the callback type is <b>IncludeThreadCallback</b>, <b>ThreadCallback</b>, or <b>ThreadExCallback</b>.

### -field SecondaryFlags

Contains a value from the <a href="/windows/win32/api/minidumpapiset/ne-minidumpapiset-minidump_secondary_flags">MINIDUMP_SECONDARY_FLAGS</a> enumeration type.

<b>DbgHelp 6.5 and earlier:  </b>This member is not available.

### -field MemoryBase

The base address of the memory region to be included in the dump. 

This member is ignored unless the callback type is <b>MemoryCallback</b> or <b>RemoveMemoryCallback</b>.

### -field MemorySize

The size of the memory region to be included in the dump, in bytes. 

This member is ignored unless the callback type is <b>MemoryCallback</b> or <b>RemoveMemoryCallback</b>.

### -field CheckCancel

Controls whether the callback function should receive cancel callbacks. If this member is <b>TRUE</b>, the cancel callbacks will continue. Otherwise, they will not.

This member is ignored unless the callback type is <b>CancelCallback</b>.

### -field Cancel

Controls whether the dump should be canceled. If the callback function returns <b>TRUE</b> and <b>Cancel</b> is <b>TRUE</b>, the dump will be canceled. In this case, the <a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function fails and the dump is not valid.

This member is ignored unless the callback type is <b>CancelCallback</b>.

### -field Handle

A handle to the file to which a kernel minidump will be written.

This member is ignored unless the callback type is <b>WriteKernelMinidumpCallback</b>.

### -field VmRegion

A <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info">MINIDUMP_MEMORY_INFO</a> structure that describes the virtual memory region. The region base and size must be aligned on a page boundary. The region size can be set to 0 to filter out the region.

This member is ignored unless the callback type is <b>IncludeVmRegionCallback</b>.

### -field Continue

Controls whether the dump should be continued. If the callback function returns <b>TRUE</b> and <b>Continue</b> is <b>TRUE</b>, the dump will be continued. Otherwise, the <a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function fails and the dump is not valid.

This member is ignored unless the callback type is <b>IncludeVmRegionCallback</b>.

### -field VmQueryStatus

### -field VmQueryResult

### -field VmReadStatus

### -field VmReadBytesCompleted

### -field Status

The status of the operation.

This member is ignored unless the callback type is <b>ReadMemoryFailureCallback</b>, <b>IoStartCallback</b>, <b>IoWriteAllCallback</b>, or <b>IoFinishCallback</b>.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-module_write_flags">MODULE_WRITE_FLAGS</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-thread_write_flags">THREAD_WRITE_FLAGS</a>