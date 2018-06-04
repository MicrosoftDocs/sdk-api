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

# D3D12_DESCRIPTOR_RANGE_FLAGS enumeration


## -description


Specifies the volatility of both descriptors and the data they reference in a Root Signature 1.1 description, which can enable some driver optimizations.


## -enum-fields




### -field D3D12_DESCRIPTOR_RANGE_FLAG_NONE

Default behavior. Descriptors are static, and default assumptions are made for data (for SRV/CBV: DATA_STATIC_WHILE_SET_AT_EXECUTE, and for UAV: DATA_VOLATILE). 


### -field D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE

If this is the only flag set, then descriptors are volatile and default assumptions are made about data (for SRV/CBV: DATA_STATIC_WHILE_SET_AT_EXECUTE, and for UAV: DATA_VOLATILE). 

If this flag is combined with DATA_VOLATILE, then both descriptors and data are volaille, which is equivalent to Root Signature Version 1.0.

If this flag is combined with DATA_STATIC_WHILE_SET_AT_EXECUTE, then descriptors are volatile. This still doesn’t allow them to change during command list execution so it is valid to combine the additional declaration that data is static while set via root descriptor table during execution – the underlying descriptors are effectively static for longer than the data is being promised to be static.


### -field D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE

Descriptors are static and the data is volatile.


### -field D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE

Descriptors are static and data is static while set at execute.


### -field D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC

Both descriptors and data are static. This maximizes the potential for driver optimization.


## -remarks



This enum is used by the  <a href="https://msdn.microsoft.com/EFC36053-6FD1-4D2E-8214-66B50F0CC0D5">D3D12_DESCRIPTOR_RANGE1</a> structure.

To specify the volatility of just the data referenced by descriptors, refer to <a href="https://msdn.microsoft.com/1BF4D1FA-C938-4704-8D82-CFCA6FE954CB">D3D12_ROOT_DESCRIPTOR_FLAGS</a>.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

