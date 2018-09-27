---
UID: NE:d3d12.D3D12_ROOT_DESCRIPTOR_FLAGS
title: D3D12_ROOT_DESCRIPTOR_FLAGS
author: windows-sdk-content
description: Specifies the volatility of the data referenced by descriptors in a Root Signature 1.1 description, which can enable some driver optimizations.
old-location: direct3d12\d3d12_root_descriptor_flags.htm
tech.root: direct3d12
ms.assetid: 1BF4D1FA-C938-4704-8D82-CFCA6FE954CB
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR_FLAGS, D3D12_ROOT_DESCRIPTOR_FLAGS enumeration, D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC, D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE, D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE, D3D12_ROOT_DESCRIPTOR_FLAG_NONE, d3d12/D3D12_ROOT_DESCRIPTOR_FLAGS, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_NONE, direct3d12.d3d12_root_descriptor_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_ROOT_DESCRIPTOR_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_DESCRIPTOR_FLAGS
req.redist: 
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
 

 

