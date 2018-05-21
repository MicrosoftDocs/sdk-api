---
UID: NS:d3d12.D3D12_RT_FORMAT_ARRAY
title: D3D12_RT_FORMAT_ARRAY
author: windows-driver-content
description: Wraps an array of render target formats.
old-location: direct3d12\d3d12_rt_format_array.htm
old-project: direct3d12
ms.assetid: 2C99BE03-868F-42F0-B631-6D5A9CEB1CB5
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: D3D12_RT_FORMAT_ARRAY, D3D12_RT_FORMAT_ARRAY structure, d3d12/D3D12_RT_FORMAT_ARRAY, direct3d12.d3d12_rt_format_array
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_RT_FORMAT_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_RT_FORMAT_ARRAY structure


## -description


Wraps an array of render target formats.


## -struct-fields




### -field RTFormats

Specifies a fixed-size array of DXGI_FORMAT values that define the format of up to 8 render targets.


### -field NumRenderTargets

Specifies the number of render target formats stored in the array.


## -remarks



This structure is primarily intended to be used when createing pipeline state stream descriptions that contain multiple contiguous render target format descriptions.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

