---
UID: NF:d3d11.ID3D11DeviceContext.CSGetShaderResources
title: ID3D11DeviceContext::CSGetShaderResources (d3d11.h)
description: Get the compute-shader resources.
helpviewer_keywords: ["8504e79a-bae1-cad5-dbaa-31ce196070b2","CSGetShaderResources","CSGetShaderResources method [Direct3D 11]","CSGetShaderResources method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSGetShaderResources method","ID3D11DeviceContext.CSGetShaderResources","ID3D11DeviceContext::CSGetShaderResources","d3d11/ID3D11DeviceContext::CSGetShaderResources","direct3d11.id3d11devicecontext_csgetshaderresources"]
old-location: direct3d11\id3d11devicecontext_csgetshaderresources.htm
tech.root: direct3d11
ms.assetid: 872dac3b-8461-4150-b51f-ce02f7356754
ms.date: 12/05/2018
ms.keywords: 8504e79a-bae1-cad5-dbaa-31ce196070b2, CSGetShaderResources, CSGetShaderResources method [Direct3D 11], CSGetShaderResources method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSGetShaderResources method, ID3D11DeviceContext.CSGetShaderResources, ID3D11DeviceContext::CSGetShaderResources, d3d11/ID3D11DeviceContext::CSGetShaderResources, direct3d11.id3d11devicecontext_csgetshaderresources
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
 - ID3D11DeviceContext::CSGetShaderResources
 - d3d11/ID3D11DeviceContext::CSGetShaderResources
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
 - ID3D11DeviceContext.CSGetShaderResources
---

# ID3D11DeviceContext::CSGetShaderResources


## -description

Get the compute-shader resources.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin getting shader resources from (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - 1).

### -param NumViews [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of resources to get from the device. Up to a maximum of 128 slots are available for shader resources (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - StartSlot).

### -param ppShaderResourceViews [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">ID3D11ShaderResourceView</a>**</b>

Array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">shader resource view</a> interfaces to be returned by the device.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>