---
UID: NF:d3d10.ID3D10Device.PSSetShaderResources
title: ID3D10Device::PSSetShaderResources (d3d10.h)
description: Bind an array of shader resources to the pixel shader stage. (ID3D10Device.PSSetShaderResources)
helpviewer_keywords: ["5c6524cb-030c-fa99-f855-ac20599cb810","ID3D10Device interface [Direct3D 10]","PSSetShaderResources method","ID3D10Device.PSSetShaderResources","ID3D10Device::PSSetShaderResources","PSSetShaderResources","PSSetShaderResources method [Direct3D 10]","PSSetShaderResources method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::PSSetShaderResources","direct3d10.id3d10device_pssetshaderresources"]
old-location: direct3d10\id3d10device_pssetshaderresources.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetshaderresources.htm
ms.date: 12/05/2018
ms.keywords: 5c6524cb-030c-fa99-f855-ac20599cb810, ID3D10Device interface [Direct3D 10],PSSetShaderResources method, ID3D10Device.PSSetShaderResources, ID3D10Device::PSSetShaderResources, PSSetShaderResources, PSSetShaderResources method [Direct3D 10], PSSetShaderResources method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSSetShaderResources, direct3d10.id3d10device_pssetshaderresources
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
 - ID3D10Device::PSSetShaderResources
 - d3d10/ID3D10Device::PSSetShaderResources
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
 - ID3D10Device.PSSetShaderResources
---

# ID3D10Device::PSSetShaderResources


## -description

Bind an array of shader resources to the <a href="/windows/desktop/direct3d11/pixel-shader-stage">pixel shader stage</a>.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to.

### -param NumViews [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources.

### -param ppShaderResourceViews [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>*</b>

Array of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">shader resource view</a> interfaces to set to the device.

## -remarks

If you bind a subresource as an input and an output, this API will fill the destination shader resource slot with <b>NULL</b>. The debug layer (when active) will alert you if this is true.

For information about creating shader-resource views, see <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
