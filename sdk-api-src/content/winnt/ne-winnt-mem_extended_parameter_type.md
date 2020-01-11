---
UID: NE:winnt.MEM_EXTENDED_PARAMETER_TYPE
title: MEM_EXTENDED_PARAMETER_TYPE (winnt.h)
description: Defines values for extended parameters used for file mapping into an address space.
old-location: base\mem_extended_parameter_type.htm
tech.root: Memory
ms.assetid: B3591D93-BAF5-4D6E-90ED-88E1C193670E
ms.date: 12/05/2018
ms.keywords: '*PMEM_EXTENDED_PARAMETER_TYPE, MEM_EXTENDED_PARAMETER_TYPE, MEM_EXTENDED_PARAMETER_TYPE enumeration, MemExtendedParameterAddressRequirements, MemExtendedParameterAttributeFlags, MemExtendedParameterInvalidType, MemExtendedParameterMax, MemExtendedParameterNumaNode, MemExtendedParameterPartitionHandle, MemExtendedParameterUserPhysicalHandle, base.mem_extended_parameter_type, winnt/MEM_EXTENDED_PARAMETER_TYPE, winnt/MemExtendedParameterAddressRequirements, winnt/MemExtendedParameterAttributeFlags, winnt/MemExtendedParameterInvalidType, winnt/MemExtendedParameterMax, winnt/MemExtendedParameterNumaNode, winnt/MemExtendedParameterPartitionHandle, winnt/MemExtendedParameterUserPhysicalHandle'
f1_keywords:
- winnt/MEM_EXTENDED_PARAMETER_TYPE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winnt.h
api_name:
- MEM_EXTENDED_PARAMETER_TYPE
targetos: Windows
req.typenames: MEM_EXTENDED_PARAMETER_TYPE, *PMEM_EXTENDED_PARAMETER_TYPE
req.redist: 
ms.custom: 19H1
---

# MEM_EXTENDED_PARAMETER_TYPE enumeration


## -description


Defines values for extended parameters used for file mapping into an address space.


## -enum-fields




### -field MemExtendedParameterInvalidType


### -field MemExtendedParameterAddressRequirements

This extended parameter type is used to specify alignment and virtual address range restrictions for new memory allocations created by <a href="https://msdn.microsoft.com/en-us/library/Mt832849(v=VS.85).aspx">VirtualAlloc2</a> and <a href="https://msdn.microsoft.com/en-us/library/Mt832844(v=VS.85).aspx">MapViewOfFile3</a>.


### -field MemExtendedParameterNumaNode

This extended parameter type is used to specify the preferred NUMA node for new memory allocations created by <a href="https://msdn.microsoft.com/en-us/library/Mt832849(v=VS.85).aspx">VirtualAlloc2</a> and <a href="https://msdn.microsoft.com/en-us/library/Mt832844(v=VS.85).aspx">MapViewOfFile3</a>.


### -field MemExtendedParameterPartitionHandle


### -field MemExtendedParameterUserPhysicalHandle


### -field MemExtendedParameterAttributeFlags


### -field MemExtendedParameterMax

