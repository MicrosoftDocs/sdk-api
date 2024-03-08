---
UID: NF:d3d10.ID3D10Device.GSGetShaderResources
title: ID3D10Device::GSGetShaderResources (d3d10.h)
description: Get the geometry shader resources. (ID3D10Device.GSGetShaderResources)
helpviewer_keywords: ["1f730e36-30d4-870c-a3ab-3a6e91123778","GSGetShaderResources","GSGetShaderResources method [Direct3D 10]","GSGetShaderResources method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GSGetShaderResources method","ID3D10Device.GSGetShaderResources","ID3D10Device::GSGetShaderResources","d3d10/ID3D10Device::GSGetShaderResources","direct3d10.id3d10device_gsgetshaderresources"]
old-location: direct3d10\id3d10device_gsgetshaderresources.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gsgetshaderresources.htm
ms.date: 12/05/2018
ms.keywords: 1f730e36-30d4-870c-a3ab-3a6e91123778, GSGetShaderResources, GSGetShaderResources method [Direct3D 10], GSGetShaderResources method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSGetShaderResources method, ID3D10Device.GSGetShaderResources, ID3D10Device::GSGetShaderResources, d3d10/ID3D10Device::GSGetShaderResources, direct3d10.id3d10device_gsgetshaderresources
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::GSGetShaderResources
 - d3d10/ID3D10Device::GSGetShaderResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GSGetShaderResources
---

# ID3D10Device::GSGetShaderResources


## -description

Get the geometry shader resources.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin getting shader resources from.

### -param NumViews [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of resources to get from the device. Up to a maximum of 128 slots are available for shader resources.

### -param ppShaderResourceViews [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>**</b>

Array of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">shader resource view</a> interfaces to be returned by the device.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
