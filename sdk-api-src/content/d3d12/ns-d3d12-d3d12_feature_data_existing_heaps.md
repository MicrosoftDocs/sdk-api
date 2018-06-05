---
UID: NS:d3d12.D3D12_FEATURE_DATA_EXISTING_HEAPS
title: D3D12_FEATURE_DATA_EXISTING_HEAPS
author: windows-sdk-content
description: Used to determinine whether the adapter supports creating heaps from existing system memory.
old-location: direct3d12\d3d12_feature_data_existing_heaps.htm
old-project: direct3d12
ms.assetid: 7F0D0FAD-BF29-43AD-95FA-85B9719C4782
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_FEATURE_DATA_EXISTING_HEAPS, D3D12_FEATURE_DATA_EXISTING_HEAPS structure, d3d12/D3D12_FEATURE_DATA_EXISTING_HEAPS, direct3d12.d3d12_feature_data_existing_heaps
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
req.typenames: D3D12_FEATURE_DATA_EXISTING_HEAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_FEATURE_DATA_EXISTING_HEAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_FEATURE_DATA_EXISTING_HEAPS structure


## -description


Used to determinine whether the adapter supports creating heaps from existing system memory. Such heaps are not intended for general use, but are exceptionally useful for diagnostic purposes because they are guaranteed to persist even after the adapter faults or experiences a device-removal event. Persistence is not guaranteed for heaps returned by CreateHeap or CreateCommittedResource, even when the heap resides in system memory.


## -struct-fields




### -field Supported

True if the adapter can create a heap from existing system memory. Otherwise, false.


## -remarks



For a variety of performance and compatibility reasons, applications should not make use of this feature except for diagnostic purposes. In particular, heaps created using this feature only support system-memory heaps with cross-adapter properties, which precludes many optimization opportunities that typical application scenarios could otherwise take advantage of.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

