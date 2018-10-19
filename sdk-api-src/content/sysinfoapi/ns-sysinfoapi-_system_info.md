---
UID: NS:sysinfoapi._SYSTEM_INFO
title: "_SYSTEM_INFO"
author: windows-sdk-content
description: Contains information about the current computer system. This includes the architecture and type of the processor, the number of processors in the system, the page size, and other such information.
old-location: base\system_info_str.htm
tech.root: sysinfo
ms.assetid: 971293b8-0af0-4bdf-a7d7-6b1bb80a469c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*LPSYSTEM_INFO, PROCESSOR_AMD_X8664, PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_ARM, PROCESSOR_ARCHITECTURE_ARM64, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, PROCESSOR_ARCHITECTURE_UNKNOWN, PROCESSOR_ARM, PROCESSOR_INTEL_386, PROCESSOR_INTEL_486, PROCESSOR_INTEL_IA64, PROCESSOR_INTEL_PENTIUM, SYSTEM_INFO, SYSTEM_INFO structure, _SYSTEM_INFO, _win32_system_info_str, base.system_info_str, sysinfoapi/_SYSTEM_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sysinfoapi.h
api_name:
 - SYSTEM_INFO
product: Windows
targetos: Windows
req.typenames: SYSTEM_INFO, *LPSYSTEM_INFO
req.redist: 
---

# _SYSTEM_INFO structure


## -description


Contains information about the current computer system. This includes the architecture and type of the processor, the number of processors in the system, the page size, and other such information.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.dwOemId

An obsolete member that is retained for compatibility. Applications should use the <b>wProcessorArchitecture</b> branch of the union.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.wProcessorArchitecture

The processor architecture of the installed operating system. This member can be one of the following values.

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
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_ARM"></a><a id="processor_architecture_arm"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_ARM</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
ARM

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_ARM64"></a><a id="processor_architecture_arm64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_ARM64</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
ARM64

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
Unknown architecture.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.wReserved

This member is reserved for future use.


### -field dwPageSize

The page size and the granularity of page protection and commitment. This is the page size used by the 
<a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> function.


### -field lpMinimumApplicationAddress

A pointer to the lowest memory address accessible to applications and dynamic-link libraries (DLLs).


### -field lpMaximumApplicationAddress

A pointer to the highest memory address accessible to applications and DLLs.


### -field dwActiveProcessorMask

 A mask representing the set of processors configured into the system. Bit 0 is processor 0; bit 31 is processor 31.


### -field dwNumberOfProcessors

The number of logical processors in the current group. To retrieve this value, use the <a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a> function.

<div class="alert"><b>Note</b>  For information about the  physical processors shared by logical processors, call <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> with the <i>RelationshipType</i> parameter set to RelationProcessorPackage (3).</div>
<div> </div>

### -field dwProcessorType

An obsolete member that is retained for compatibility. Use the <b>wProcessorArchitecture</b>, <b>wProcessorLevel</b>, and <b>wProcessorRevision</b> members to determine the type of processor.
						
					



#### PROCESSOR_INTEL_386 (386)



#### PROCESSOR_INTEL_486 (486)



#### PROCESSOR_INTEL_PENTIUM (586)



#### PROCESSOR_INTEL_IA64 (2200)



#### PROCESSOR_AMD_X8664 (8664)



#### PROCESSOR_ARM (Reserved)


### -field dwAllocationGranularity

The granularity for the starting address at which virtual memory can be allocated. For more information, see <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>.


### -field wProcessorLevel

The architecture-dependent processor level. It should be used only for display purposes. To determine the feature set of a processor, use the 
<a href="https://msdn.microsoft.com/c58cfb0a-f40f-429c-abe9-83b6f038f612">IsProcessorFeaturePresent</a> function.

If <b>wProcessorArchitecture</b> is PROCESSOR_ARCHITECTURE_INTEL, <b>wProcessorLevel</b> is defined by the CPU vendor.

If <b>wProcessorArchitecture</b> is PROCESSOR_ARCHITECTURE_IA64, <b>wProcessorLevel</b> is set to 1.


### -field wProcessorRevision

The architecture-dependent processor revision. The following table shows how the revision value is assembled for each type of processor architecture. 



<table>
<tr>
<th>Processor</th>
<th>Value</th>
</tr>
<tr>
<td>Intel Pentium, Cyrix, or NextGen 586</td>
<td>The high byte is the model and the low byte is the stepping. For example, if the value is <i>xxyy</i>, the model number and stepping can be displayed as follows: 


Model <i>xx</i>, Stepping <i>yy</i>

</td>
</tr>
<tr>
<td>Intel 80386 or 80486</td>
<td>A value of the form <i>xxyz</i>. 


If <i>xx</i> is equal to 0xFF, <i>y</i> - 0xA is the model number, and <i>z</i> is the stepping identifier.

If <i>xx</i> is not equal to 0xFF, <i>xx</i> + 'A' is the stepping letter and <i>yz</i> is the minor stepping.

</td>
</tr>
<tr>
<td>ARM</td>
<td>Reserved.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/a4a1123b-83d7-4ee2-aa38-68fff5373618">GetNativeSystemInfo</a>



<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/2ac8a7d6-5c52-41de-acb9-d7f975fd2a94">MapViewOfFileEx</a>
 

 

