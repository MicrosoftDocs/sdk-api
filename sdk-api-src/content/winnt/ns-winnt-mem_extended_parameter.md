---
UID: NS:winnt.MEM_EXTENDED_PARAMETER
title: MEM_EXTENDED_PARAMETER
author: windows-sdk-content
description: Represents an extended parameter for a function that manages virtual memory.
old-location: base\mem_extended_parameter.htm
tech.root: Memory
ms.assetid: 8D189F7E-83E7-4AF3-9E25-928C66666887
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: "*PMEM_EXTENDED_PARAMETER, MEM_EXTENDED_PARAMETER, MEM_EXTENDED_PARAMETER structure, PMEM_EXTENDED_PARAMETER, PMEM_EXTENDED_PARAMETER structure pointer, base.mem_extended_parameter, winnt/MEM_EXTENDED_PARAMETER, winnt/PMEM_EXTENDED_PARAMETER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - MEM_EXTENDED_PARAMETER
product: Windows
targetos: Windows
req.typenames: MEM_EXTENDED_PARAMETER, *PMEM_EXTENDED_PARAMETER
req.redist: 
---

# MEM_EXTENDED_PARAMETER structure


## -description


Represents an extended parameter for a function that manages virtual memory.


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.Type

A <a href="base.mem_extended_parameter_type">MEM_EXTENDED_PARAMETER_TYPE</a> value that indicates the type of the parameter.

If <i>Type</i> is set to <b>MemExtendedParameterAddressRequirements</b>, then <i>Pointer</i> must be a pointer to a caller-allocated <a href="base.mem_address_requirements">MEM_ADDRESS_REQUIREMENTS</a> structure that specifies the lowest and highest base address and alignment.

If <i>Type</i> is set to <b>MemExtendedParameterNumaNode</b>, then <i>ULong</i> must be set to the desired node number.


### -field DUMMYSTRUCTNAME.Reserved

Reserved.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ULong64


### -field DUMMYUNIONNAME.Pointer

If <i>Type</i> is set to <b>MemExtendedParameterAddressRequirements</b>, then <i>Pointer</i> must be a pointer to a caller-allocated <a href="base.mem_address_requirements">MEM_ADDRESS_REQUIREMENTS</a> structure that specifies the lowest and highest base address and alignment.


### -field DUMMYUNIONNAME.Size


### -field DUMMYUNIONNAME.Handle


### -field DUMMYUNIONNAME.ULong

If <i>Type</i> is set to <b>MemExtendedParameterNumaNode</b>, then <i>ULong</i> must be set to the desired node number.

