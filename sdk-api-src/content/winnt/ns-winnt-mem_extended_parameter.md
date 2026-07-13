---
UID: NS:winnt.MEM_EXTENDED_PARAMETER
title: MEM_EXTENDED_PARAMETER (winnt.h)
description: Represents an extended parameter for a function that manages virtual memory.
helpviewer_keywords: ["*PMEM_EXTENDED_PARAMETER","MEM_EXTENDED_PARAMETER","MEM_EXTENDED_PARAMETER structure","PMEM_EXTENDED_PARAMETER","PMEM_EXTENDED_PARAMETER structure pointer","base.mem_extended_parameter","winnt/MEM_EXTENDED_PARAMETER","winnt/PMEM_EXTENDED_PARAMETER"]
old-location: base\mem_extended_parameter.htm
tech.root: base
ms.assetid: 8D189F7E-83E7-4AF3-9E25-928C66666887
ms.date: 12/05/2018
ms.keywords: '*PMEM_EXTENDED_PARAMETER, MEM_EXTENDED_PARAMETER, MEM_EXTENDED_PARAMETER structure, PMEM_EXTENDED_PARAMETER, PMEM_EXTENDED_PARAMETER structure pointer, base.mem_extended_parameter, winnt/MEM_EXTENDED_PARAMETER, winnt/PMEM_EXTENDED_PARAMETER'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: MEM_EXTENDED_PARAMETER, *PMEM_EXTENDED_PARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MEM_EXTENDED_PARAMETER
 - winnt/MEM_EXTENDED_PARAMETER
 - PMEM_EXTENDED_PARAMETER
 - winnt/PMEM_EXTENDED_PARAMETER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - MEM_EXTENDED_PARAMETER
---

# MEM_EXTENDED_PARAMETER structure


## -description

Represents an extended parameter for a function that manages virtual memory.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.Type

A <a href="../winnt/ne-winnt-mem_extended_parameter_type.md">MEM_EXTENDED_PARAMETER_TYPE</a> value that indicates the type of the parameter.


If <i>Type</i> is set to <b>MemExtendedParameterAddressRequirements</b>, then <i>Pointer</i> must be a pointer to a caller-allocated <a href="ns-winnt-mem_address_requirements.md">MEM_ADDRESS_REQUIREMENTS</a> structure that specifies the lowest and highest base address and alignment.

If <i>Type</i> is set to <b>MemExtendedParameterNumaNode</b>, then <i>ULong64</i> must be set to the desired node number.

If <i>Type</i> is set to <b>MemExtendedParameterAttributeFlags</b>, then <i>ULong64</i> must be set to a value that contains the desired flags:
 
<table>
<thead>
<tr>
<th>Flag</th>
 <th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr>
<td>MEM_EXTENDED_PARAMETER_NONPAGED</td>
<td>0x02</td>
<td>The allocation is non-pageable.</td>
</tr>
<tr>
<tr>
<td>MEM_EXTENDED_PARAMETER_NONPAGED_LARGE</td>
<td>0x08</td>
<td>The allocation is mapped using large pages.</td>
</tr>
<tr>
<td>MEM_EXTENDED_PARAMETER_NONPAGED_HUGE</td>
<td>0x10</td>
<td>The allocation is mapped using huge pages.</td>
</tr>
<tr>
<td>MEM_EXTENDED_PARAMETER_EC_CODE</td>
<td>0x40</td>
<td>The allocation will contain <a href="https://docs.microsoft.com/en-us/windows/arm/arm64ec">emulation-compatible (EC)</a> code.</td>
</tr>
</tbody>
</table>


### -field DUMMYSTRUCTNAME.Reserved

Reserved.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.ULong64

If <i>Type</i> is set to <b>MemExtendedParameterNumaNode</b>, then <i>ULong64</i> must be set to the desired node number.

### -field DUMMYUNIONNAME.Pointer


If <i>Type</i> is set to <b>MemExtendedParameterAddressRequirements</b>, then <i>Pointer</i> must be a pointer to a caller-allocated <a href="ns-winnt-mem_address_requirements.md">MEM_ADDRESS_REQUIREMENTS</a> structure that specifies the lowest and highest base address and alignment.


### -field DUMMYUNIONNAME.Size

### -field DUMMYUNIONNAME.Handle

### -field DUMMYUNIONNAME.ULong
