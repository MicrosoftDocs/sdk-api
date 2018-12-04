---
UID: NS:d3d12.D3D12_FEATURE_DATA_EXISTING_HEAPS
title: D3D12_FEATURE_DATA_EXISTING_HEAPS
author: windows-sdk-content
description: Provides detail about whether the adapter supports creating heaps from existing system memory.
old-location: direct3d12\d3d12_feature_data_existing_heaps.htm
tech.root: direct3d12
ms.assetid: 7F0D0FAD-BF29-43AD-95FA-85B9719C4782
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D3D12_FEATURE_DATA_EXISTING_HEAPS, D3D12_FEATURE_DATA_EXISTING_HEAPS structure, d3d12/D3D12_FEATURE_DATA_EXISTING_HEAPS, direct3d12.d3d12_feature_data_existing_heaps
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D12_FEATURE_DATA_EXISTING_HEAPS
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_EXISTING_HEAPS
req.redist: 
---

# D3D12_FEATURE_DATA_EXISTING_HEAPS structure


## -description


Provides detail about whether the adapter supports creating heaps from existing system memory. Such heaps are not intended for general use, but are exceptionally useful for diagnostic purposes, because they are guaranteed to persist even after the adapter faults or experiences a device-removal event. Persistence is not guaranteed for heaps returned by <a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">ID3D12Device::CreateHeap</a> or <a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">ID3D12Device::CreateCommittedResource</a>, even when the heap resides in system memory.


## -struct-fields




### -field Supported

<b>TRUE</b> if the adapter can create a heap from existing system memory. Otherwise, <b>FALSE</b>.


## -remarks



For a variety of performance and compatibility reasons, applications should not make use of this feature except for diagnostic purposes. In particular, heaps created using this feature only support system-memory heaps with cross-adapter properties, which precludes many optimization opportunities that typical application scenarios could otherwise take advantage of.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>



<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">ID3D12Device::CreateCommittedResource</a>



<a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">ID3D12Device::CreateHeap</a>
 

 

