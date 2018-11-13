---
UID: NS:d3d12.D3D12_CONSTANT_BUFFER_VIEW_DESC
title: D3D12_CONSTANT_BUFFER_VIEW_DESC
author: windows-sdk-content
description: Describes a constant buffer to view.
old-location: direct3d12\d3d12_constant_buffer_view_desc.htm
tech.root: direct3d12
ms.assetid: 83A4522E-AE87-42CE-9B95-CF63E92556AD
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_CONSTANT_BUFFER_VIEW_DESC, D3D12_CONSTANT_BUFFER_VIEW_DESC structure, d3d12/D3D12_CONSTANT_BUFFER_VIEW_DESC, direct3d12.d3d12_constant_buffer_view_desc
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_CONSTANT_BUFFER_VIEW_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_CONSTANT_BUFFER_VIEW_DESC
req.redist: 
---

# D3D12_CONSTANT_BUFFER_VIEW_DESC structure


## -description


Describes a constant buffer to view.


## -struct-fields




### -field BufferLocation

The D3D12_GPU_VIRTUAL_ADDRESS of the constant buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.
          


### -field SizeInBytes

The size in bytes of the constant buffer.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/13251F82-4AE9-4234-A0C8-0E666F8A1856">CreateConstantBufferView</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

