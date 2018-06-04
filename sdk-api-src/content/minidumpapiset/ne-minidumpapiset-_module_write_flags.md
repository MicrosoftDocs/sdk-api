---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MODULE_WRITE_FLAGS enumeration


## -description


Identifies the type of module information that will be written to the minidump file by the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function.


## -enum-fields




### -field ModuleWriteModule

Only module information will be written to the minidump file.


### -field ModuleWriteDataSeg

Module and data segment information will be written to the minidump file. This value will only be set if the <b>MiniDumpWithDataSegs</b> enumeration value from <a href="https://msdn.microsoft.com/89ae3a75-5f02-4c5e-9d72-95fb8ef94985">MINIDUMP_TYPE</a> is set.


### -field ModuleWriteMiscRecord

Module, data segment, and miscellaneous record information will be written to the minidump file.


### -field ModuleWriteCvRecord

CodeView information will be written to the minidump file. Some debuggers need the CodeView information to properly locate symbols.


### -field ModuleReferencedByMemory

Indicates that a module was referenced by a pointer on the stack or backing store of a thread in the minidump. This value is valid only if the <i>DumpType</i> parameter of the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function includes <b>MiniDumpScanMemory</b>.


### -field ModuleWriteTlsData

Per-module automatic TLS data is written to the minidump file. (Note that automatic TLS data is created using <b>__declspec(thread)</b> while <a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a> creates dynamic TLS data). This value is valid only if the <i>DumpType</i> parameter of the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function includes <b>MiniDumpWithProcessThreadData</b>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.


### -field ModuleWriteCodeSegs

Code segment information will be written to the minidump file. This value will only be set if the <b>MiniDumpWithCodeSegs</b> enumeration value from <a href="https://msdn.microsoft.com/89ae3a75-5f02-4c5e-9d72-95fb8ef94985">MINIDUMP_TYPE</a> is set.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.


## -see-also




<a href="https://msdn.microsoft.com/57949087-0f22-40c8-ab56-326a8304c310">MINIDUMP_CALLBACK_OUTPUT</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

