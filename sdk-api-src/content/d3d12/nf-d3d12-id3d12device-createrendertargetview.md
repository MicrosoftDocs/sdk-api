---
UID: NF:d3d12.ID3D12Device.CreateRenderTargetView
title: ID3D12Device::CreateRenderTargetView
author: windows-sdk-content
description: Creates a render-target view for accessing resource data.
old-location: direct3d12\id3d12device_createrendertargetview.htm
tech.root: direct3d12
ms.assetid: B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateRenderTargetView, CreateRenderTargetView method, CreateRenderTargetView method,ID3D12Device interface, ID3D12Device interface,CreateRenderTargetView method, ID3D12Device.CreateRenderTargetView, ID3D12Device::CreateRenderTargetView, d3d12/ID3D12Device::CreateRenderTargetView, direct3d12.id3d12device_createrendertargetview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateRenderTargetView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateRenderTargetView


## -description


Creates a render-target view for accessing resource data.


## -parameters




### -param pResource [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a> object that represents the render target.
          

At least one of <i>pResource</i> or <i>pDesc</i>  must be provided.
A null <i>pResource</i> is used to initialize a null descriptor, which guarantees D3D11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.



### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn770389(v=VS.85).aspx">D3D12_RENDER_TARGET_VIEW_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn770389(v=VS.85).aspx">D3D12_RENDER_TARGET_VIEW_DESC</a> structure that describes the render-target view.

A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and RTVs target the first mip and all array slices. Not all resources support null descriptor initialization.


### -param DestDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn859369(v=VS.85).aspx">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the render-target view.
          


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>
 

 

