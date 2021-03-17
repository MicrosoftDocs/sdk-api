---
UID: NF:d3d11.ID3D11DeviceContext.CSSetShaderResources
title: ID3D11DeviceContext::CSSetShaderResources (d3d11.h)
description: Bind an array of shader resources to the compute-shader stage.
helpviewer_keywords: ["CSSetShaderResources","CSSetShaderResources method [Direct3D 11]","CSSetShaderResources method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSSetShaderResources method","ID3D11DeviceContext.CSSetShaderResources","ID3D11DeviceContext::CSSetShaderResources","cef14155-2203-ea99-84d2-f1722c5ae802","d3d11/ID3D11DeviceContext::CSSetShaderResources","direct3d11.id3d11devicecontext_cssetshaderresources"]
old-location: direct3d11\id3d11devicecontext_cssetshaderresources.htm
tech.root: direct3d11
ms.assetid: 04babe17-b053-49f4-90bc-8080f521079e
ms.date: 12/05/2018
ms.keywords: CSSetShaderResources, CSSetShaderResources method [Direct3D 11], CSSetShaderResources method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSSetShaderResources method, ID3D11DeviceContext.CSSetShaderResources, ID3D11DeviceContext::CSSetShaderResources, cef14155-2203-ea99-84d2-f1722c5ae802, d3d11/ID3D11DeviceContext::CSSetShaderResources, direct3d11.id3d11devicecontext_cssetshaderresources
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
 - ID3D11DeviceContext::CSSetShaderResources
 - d3d11/ID3D11DeviceContext::CSSetShaderResources
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
 - ID3D11DeviceContext.CSSetShaderResources
---

# ID3D11DeviceContext::CSSetShaderResources


## -description

Bind an array of shader resources to the compute-shader stage.

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