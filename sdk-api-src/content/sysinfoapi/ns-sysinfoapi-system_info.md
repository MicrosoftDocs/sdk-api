---
UID: NS:sysinfoapi._SYSTEM_INFO
title: SYSTEM_INFO (sysinfoapi.h)
description: Contains information about the current computer system. This includes the architecture and type of the processor, the number of processors in the system, the page size, and other such information.
helpviewer_keywords: ["*LPSYSTEM_INFO","PROCESSOR_AMD_X8664","PROCESSOR_ARCHITECTURE_AMD64","PROCESSOR_ARCHITECTURE_ARM","PROCESSOR_ARCHITECTURE_ARM64","PROCESSOR_ARCHITECTURE_IA64","PROCESSOR_ARCHITECTURE_INTEL","PROCESSOR_ARCHITECTURE_UNKNOWN","PROCESSOR_ARM","PROCESSOR_INTEL_386","PROCESSOR_INTEL_486","PROCESSOR_INTEL_IA64","PROCESSOR_INTEL_PENTIUM","SYSTEM_INFO","SYSTEM_INFO structure","_SYSTEM_INFO","_win32_system_info_str","base.system_info_str","sysinfoapi/_SYSTEM_INFO"]
old-location: base\system_info_str.htm
tech.root: winprog
ms.assetid: 971293b8-0af0-4bdf-a7d7-6b1bb80a469c
ms.date: 12/05/2018
ms.keywords: '*LPSYSTEM_INFO, PROCESSOR_AMD_X8664, PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_ARM, PROCESSOR_ARCHITECTURE_ARM64, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, PROCESSOR_ARCHITECTURE_UNKNOWN, PROCESSOR_ARM, PROCESSOR_INTEL_386, PROCESSOR_INTEL_486, PROCESSOR_INTEL_IA64, PROCESSOR_INTEL_PENTIUM, SYSTEM_INFO, SYSTEM_INFO structure, _SYSTEM_INFO, _win32_system_info_str, base.system_info_str, sysinfoapi/_SYSTEM_INFO'
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
targetos: Windows
req.typenames: SYSTEM_INFO, *LPSYSTEM_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_INFO
 - sysinfoapi/_SYSTEM_INFO
 - LPSYSTEM_INFO
 - sysinfoapi/LPSYSTEM_INFO
 - SYSTEM_INFO
 - sysinfoapi/SYSTEM_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sysinfoapi.h
api_name:
 - SYSTEM_INFO
---

# SYSTEM_INFO structure


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
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function.

### -field lpMinimumApplicationAddress

A pointer to the lowest memory address accessible to applications and dynamic-link libraries (DLLs).

### -field lpMaximumApplicationAddress

A pointer to the highest memory address accessible to applications and DLLs.

### -field dwActiveProcessorMask

 A mask representing the set of processors configured into the system. Bit 0 is processor 0; bit 31 is processor 31.

### -field dwNumberOfProcessors

The number of logical processors in the current group. To retrieve the current processor group, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation">GetLogicalProcessorInformation</a> function.

<div class="alert"><b>Note</b>  For information about the  physical processors shared by logical processors, call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> with the <i>RelationshipType</i> parameter set to RelationProcessorPackage (3).</div>
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

The granularity for the starting address at which virtual memory can be allocated. For more information, see <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>.

### -field wProcessorLevel

The architecture-dependent processor level. It should be used only for display purposes. To determine the feature set of a processor, use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent">IsProcessorFeaturePresent</a> function.

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

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>
