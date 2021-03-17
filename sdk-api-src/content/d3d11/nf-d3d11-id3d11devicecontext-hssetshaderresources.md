---
UID: NF:d3d11.ID3D11DeviceContext.HSSetShaderResources
title: ID3D11DeviceContext::HSSetShaderResources (d3d11.h)
description: Bind an array of shader resources to the hull-shader stage.
helpviewer_keywords: ["HSSetShaderResources","HSSetShaderResources method [Direct3D 11]","HSSetShaderResources method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","HSSetShaderResources method","ID3D11DeviceContext.HSSetShaderResources","ID3D11DeviceContext::HSSetShaderResources","d3d11/ID3D11DeviceContext::HSSetShaderResources","direct3d11.id3d11devicecontext_hssetshaderresources","e7e39206-8761-2097-5503-d31d970dd578"]
old-location: direct3d11\id3d11devicecontext_hssetshaderresources.htm
tech.root: direct3d11
ms.assetid: cb99cb22-a7e4-4472-b519-12bced9a45b8
ms.date: 12/05/2018
ms.keywords: HSSetShaderResources, HSSetShaderResources method [Direct3D 11], HSSetShaderResources method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],HSSetShaderResources method, ID3D11DeviceContext.HSSetShaderResources, ID3D11DeviceContext::HSSetShaderResources, d3d11/ID3D11DeviceContext::HSSetShaderResources, direct3d11.id3d11devicecontext_hssetshaderresources, e7e39206-8761-2097-5503-d31d970dd578
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::HSSetShaderResources
 - d3d11/ID3D11DeviceContext::HSSetShaderResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.HSSetShaderResources
---

# ID3D11DeviceContext::HSSetShaderResources


## -description

Bind an array of shader resources to the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - 1).

### -param NumViews [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources(ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - StartSlot).

### -param ppShaderResourceViews [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">ID3D11ShaderResourceView</a>*</b>

Array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">shader resource view</a> interfaces to set to the device.

## -remarks

If an overlapping resource view is already bound to an output slot, such as a render target, then the method will fill the destination shader resource slot with <b>NULL</b>.

For information about creating shader-resource views, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>