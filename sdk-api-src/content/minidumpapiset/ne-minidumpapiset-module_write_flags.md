---
UID: NE:minidumpapiset._MODULE_WRITE_FLAGS
title: MODULE_WRITE_FLAGS (minidumpapiset.h)
description: Identifies the type of module information that will be written to the minidump file by the MiniDumpWriteDump function.
helpviewer_keywords: ["MODULE_WRITE_FLAGS","MODULE_WRITE_FLAGS enumeration","ModuleReferencedByMemory","ModuleWriteCodeSegs","ModuleWriteCvRecord","ModuleWriteDataSeg","ModuleWriteMiscRecord","ModuleWriteModule","ModuleWriteTlsData","_win32_module_write_flags","base.module_write_flags","minidumpapiset/MODULE_WRITE_FLAGS","minidumpapiset/ModuleReferencedByMemory","minidumpapiset/ModuleWriteCodeSegs","minidumpapiset/ModuleWriteCvRecord","minidumpapiset/ModuleWriteDataSeg","minidumpapiset/ModuleWriteMiscRecord","minidumpapiset/ModuleWriteModule","minidumpapiset/ModuleWriteTlsData"]
old-location: base\module_write_flags.htm
tech.root: Debug
ms.assetid: f074edb2-2cd7-44f6-994b-c649201c1e9d
ms.date: 12/05/2018
ms.keywords: MODULE_WRITE_FLAGS, MODULE_WRITE_FLAGS enumeration, ModuleReferencedByMemory, ModuleWriteCodeSegs, ModuleWriteCvRecord, ModuleWriteDataSeg, ModuleWriteMiscRecord, ModuleWriteModule, ModuleWriteTlsData, _win32_module_write_flags, base.module_write_flags, minidumpapiset/MODULE_WRITE_FLAGS, minidumpapiset/ModuleReferencedByMemory, minidumpapiset/ModuleWriteCodeSegs, minidumpapiset/ModuleWriteCvRecord, minidumpapiset/ModuleWriteDataSeg, minidumpapiset/ModuleWriteMiscRecord, minidumpapiset/ModuleWriteModule, minidumpapiset/ModuleWriteTlsData
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
req.typenames: MODULE_WRITE_FLAGS
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MODULE_WRITE_FLAGS
 - minidumpapiset/_MODULE_WRITE_FLAGS
 - MODULE_WRITE_FLAGS
 - minidumpapiset/MODULE_WRITE_FLAGS
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
 - MODULE_WRITE_FLAGS
---

# MODULE_WRITE_FLAGS enumeration


## -description

Identifies the type of module information that will be written to the minidump file by the 
<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.

## -enum-fields

### -field ModuleWriteModule:0x0001

Only module information will be written to the minidump file.

### -field ModuleWriteDataSeg:0x0002

Module and data segment information will be written to the minidump file. This value will only be set if the <b>MiniDumpWithDataSegs</b> enumeration value from <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type">MINIDUMP_TYPE</a> is set.

### -field ModuleWriteMiscRecord:0x0004

Module, data segment, and miscellaneous record information will be written to the minidump file.

### -field ModuleWriteCvRecord:0x0008

CodeView information will be written to the minidump file. Some debuggers need the CodeView information to properly locate symbols.

### -field ModuleReferencedByMemory:0x0010

Indicates that a module was referenced by a pointer on the stack or backing store of a thread in the minidump. This value is valid only if the <i>DumpType</i> parameter of the 
<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function includes <b>MiniDumpScanMemory</b>.

### -field ModuleWriteTlsData:0x0020

Per-module automatic TLS data is written to the minidump file. (Note that automatic TLS data is created using <b>__declspec(thread)</b> while <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc">TlsAlloc</a> creates dynamic TLS data). This value is valid only if the <i>DumpType</i> parameter of the 
<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function includes <b>MiniDumpWithProcessThreadData</b>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field ModuleWriteCodeSegs:0x0040

Code segment information will be written to the minidump file. This value will only be set if the <b>MiniDumpWithCodeSegs</b> enumeration value from <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type">MINIDUMP_TYPE</a> is set.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a>



<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>
