---
UID: NE:winnt.MEM_EXTENDED_PARAMETER_TYPE
title: MEM_EXTENDED_PARAMETER_TYPE (winnt.h)
description: Defines values for extended parameters used for file mapping into an address space.
helpviewer_keywords: ["*PMEM_EXTENDED_PARAMETER_TYPE","MEM_EXTENDED_PARAMETER_TYPE","MEM_EXTENDED_PARAMETER_TYPE enumeration","MemExtendedParameterAddressRequirements","MemExtendedParameterAttributeFlags","MemExtendedParameterInvalidType","MemExtendedParameterMax","MemExtendedParameterNumaNode","MemExtendedParameterPartitionHandle","MemExtendedParameterUserPhysicalHandle","base.mem_extended_parameter_type","winnt/MEM_EXTENDED_PARAMETER_TYPE","winnt/MemExtendedParameterAddressRequirements","winnt/MemExtendedParameterAttributeFlags","winnt/MemExtendedParameterInvalidType","winnt/MemExtendedParameterMax","winnt/MemExtendedParameterNumaNode","winnt/MemExtendedParameterPartitionHandle","winnt/MemExtendedParameterUserPhysicalHandle"]
old-location: base\mem_extended_parameter_type.htm
tech.root: base
ms.assetid: B3591D93-BAF5-4D6E-90ED-88E1C193670E
ms.date: 12/05/2018
ms.keywords: '*PMEM_EXTENDED_PARAMETER_TYPE, MEM_EXTENDED_PARAMETER_TYPE, MEM_EXTENDED_PARAMETER_TYPE enumeration, MemExtendedParameterAddressRequirements, MemExtendedParameterAttributeFlags, MemExtendedParameterInvalidType, MemExtendedParameterMax, MemExtendedParameterNumaNode, MemExtendedParameterPartitionHandle, MemExtendedParameterUserPhysicalHandle, base.mem_extended_parameter_type, winnt/MEM_EXTENDED_PARAMETER_TYPE, winnt/MemExtendedParameterAddressRequirements, winnt/MemExtendedParameterAttributeFlags, winnt/MemExtendedParameterInvalidType, winnt/MemExtendedParameterMax, winnt/MemExtendedParameterNumaNode, winnt/MemExtendedParameterPartitionHandle, winnt/MemExtendedParameterUserPhysicalHandle'
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
req.typenames: MEM_EXTENDED_PARAMETER_TYPE, *PMEM_EXTENDED_PARAMETER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MEM_EXTENDED_PARAMETER_TYPE
 - winnt/MEM_EXTENDED_PARAMETER_TYPE
 - PMEM_EXTENDED_PARAMETER_TYPE
 - winnt/PMEM_EXTENDED_PARAMETER_TYPE
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
 - MEM_EXTENDED_PARAMETER_TYPE
---

# MEM_EXTENDED_PARAMETER_TYPE enumeration


## -description

Defines values for extended parameters used for file mapping into an address space.

## -enum-fields

### -field MemExtendedParameterInvalidType:0

### -field MemExtendedParameterAddressRequirements

This extended parameter type is used to specify alignment and virtual address range restrictions for new memory allocations created by <a href="../memoryapi/nf-memoryapi-virtualalloc2.md">VirtualAlloc2</a> and <a href="../memoryapi/nf-memoryapi-mapviewoffile3.md">MapViewOfFile3</a>.

### -field MemExtendedParameterNumaNode

This extended parameter type is used to specify the preferred NUMA node for new memory allocations created by <a href="../memoryapi/nf-memoryapi-virtualalloc2.md">VirtualAlloc2</a> and <a href="../memoryapi/nf-memoryapi-mapviewoffile3.md">MapViewOfFile3</a>.

### -field MemExtendedParameterPartitionHandle

### -field MemExtendedParameterUserPhysicalHandle

### -field MemExtendedParameterAttributeFlags

### -field MemExtendedParameterMax

