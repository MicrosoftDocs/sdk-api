---
UID: NS:d3d12.D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
title: D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
author: windows-sdk-content
description: Details the adapter's GPU virtual address space limitations, including maximum address bits per resource and per process.
old-location: direct3d12\d3d12_feature_data_gpu_virtual_address_support.htm
old-project: direct3d12
ms.assetid: 2CBED491-A8B6-47AE-8371-2081BAF85B83
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure, d3d12/D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT, direct3d12.d3d12_feature_data_gpu_virtual_address_support
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure


## -description



          Details the adapter's GPU virtual address space limitations, including maximum address bits per resource and per process.
        


## -struct-fields




### -field MaxGPUVirtualAddressBitsPerResource

The maximum GPU virtual address bits per resource.

Some adapters have significantly less bits available per resource than per process, while other adapters have significantly greater bits available per resource than per process. The latter scenario tends to happen in less common scenarios, like when running a 32-bit process on certain UMA adapters.
When per resource capabilities are greater than per process, the greater per resource capabilities can only be leveraged by reserved resources or NULL mapped pages.



### -field MaxGPUVirtualAddressBitsPerProcess


            The maximum GPU virtual address bits per process.

When this value is nearly equal to the available residency budget, <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a> will not be a feasible option to manage residency. See <a href="https://msdn.microsoft.com/2B3B97DC-5AA3-470E-8EED-3956B295BB94">MakeResident</a> for more details.


## -remarks




        See the enumeration constant D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT in the <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a> enumeration.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

