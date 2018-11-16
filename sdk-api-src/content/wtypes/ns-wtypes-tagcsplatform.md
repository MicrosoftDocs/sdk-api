---
UID: NS:wtypes.tagCSPLATFORM
title: tagCSPLATFORM
author: windows-sdk-content
description: Defines an operating system platform and process architecture.
old-location: winprog\csplatform.htm
tech.root: DevNotes
ms.assetid: cb8b4615-427d-4277-ad4b-c9988c3e1be7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CSPLATFORM, CSPLATFORM structure [Windows API], PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, PROCESSOR_ARCHITECTURE_UNKNOWN, tagCSPLATFORM, winprog.csplatform, wtypes/tagCSPLATFORM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypes.h
api_name:
 - CSPLATFORM
product: Windows
targetos: Windows
req.typenames: CSPLATFORM
req.redist: 
---

# tagCSPLATFORM structure


## -description


Defines an operating system platform and process architecture.


## -struct-fields




### -field dwPlatformId

 


### -field dwVersionHi

The major version of the operating system.


### -field dwVersionLo

The minor version of the operating system.


### -field dwProcessorArch

The processor architecture.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_AMD64"></a><a id="processor_architecture_amd64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_AMD64</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
x64 (AMD or Intel)

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_IA64"></a><a id="processor_architecture_ia64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_IA64</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Intel Itanium-based

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_INTEL"></a><a id="processor_architecture_intel"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_INTEL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
x86

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_UNKNOWN"></a><a id="processor_architecture_unknown"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_UNKNOWN</b></dt>
<dt>0xffff</dt>
</dl>
</td>
<td width="60%">
Unknown processor.

</td>
</tr>
</table>
 


#### - dwContext

The operating system platform (VER_PLATFORM_WIN32_NT).


## -see-also




<a href="https://msdn.microsoft.com/8b27c090-2bae-4511-9be8-4bc077295ac5">QUERYCONTEXT</a>
 

 

