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

# D3D12_ROOT_DESCRIPTOR_FLAGS enumeration


## -description


Specifies the volatility of the data referenced by descriptors in a Root Signature 1.1 description, which can enable some driver optimizations.


## -enum-fields




### -field D3D12_ROOT_DESCRIPTOR_FLAG_NONE

Default assumptions are made for data (for SRV/CBV: DATA_STATIC_WHILE_SET_AT_EXECUTE, and for UAV: DATA_VOLATILE). 


### -field D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE

Data is volatile. Equivalent to Root Signature Version 1.0.


### -field D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE

Data is static while set at execute.


### -field D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC

Data is static. The best potential for driver optimization.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/55627E99-6EED-442F-93B8-D869F0B4EAF4">D3D12_ROOT_DESCRIPTOR1</a> structure.

To specify the volatility of both descriptors and data, refer to <a href="https://msdn.microsoft.com/B22DBE80-A0BE-40F9-ADC2-5AFB35DDDDE8">D3D12_DESCRIPTOR_RANGE_FLAGS</a>. 




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

