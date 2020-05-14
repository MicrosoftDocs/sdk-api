---
UID: NF:d3d10.ID3D10Device.PSGetShaderResources
title: ID3D10Device::PSGetShaderResources (d3d10.h)
description: Get the pixel shader resources.helpviewer_keywords: ["54b6aa73-f39a-9734-0be4-f47362f38b2f","ID3D10Device interface [Direct3D 10]","PSGetShaderResources method","ID3D10Device.PSGetShaderResources","ID3D10Device::PSGetShaderResources","PSGetShaderResources","PSGetShaderResources method [Direct3D 10]","PSGetShaderResources method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::PSGetShaderResources","direct3d10.id3d10device_psgetshaderresources"]
old-location: direct3d10\id3d10device_psgetshaderresources.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_psgetshaderresources.htm
ms.date: 12/05/2018
ms.keywords: 54b6aa73-f39a-9734-0be4-f47362f38b2f, ID3D10Device interface [Direct3D 10],PSGetShaderResources method, ID3D10Device.PSGetShaderResources, ID3D10Device::PSGetShaderResources, PSGetShaderResources, PSGetShaderResources method [Direct3D 10], PSGetShaderResources method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSGetShaderResources, direct3d10.id3d10device_psgetshaderresources
f1_keywords:
- d3d10/ID3D10Device.PSGetShaderResources
dev_langs:
- c++
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10.lib
- D3D10.dll
api_name:
- ID3D10Device.PSGetShaderResources
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::PSGetShaderResources


## -description


Get the pixel shader resources.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin getting shader resources from.


### -param NumViews [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of resources to get from the device. Up to a maximum of 128 slots are available for shader resources.


### -param ppShaderResourceViews [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>**</b>

Array of <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">shader resource view</a> interfaces to be returned by the device.


## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

