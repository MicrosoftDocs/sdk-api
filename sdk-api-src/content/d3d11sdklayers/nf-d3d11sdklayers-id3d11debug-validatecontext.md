---
UID: NF:d3d11sdklayers.ID3D11Debug.ValidateContext
title: ID3D11Debug::ValidateContext (d3d11sdklayers.h)
description: Check to see if the draw pipeline state is valid.
helpviewer_keywords: ["4ee713bf-94e0-0a30-fb72-d6e8a2216e88","ID3D11Debug interface [Direct3D 11]","ValidateContext method","ID3D11Debug.ValidateContext","ID3D11Debug::ValidateContext","ValidateContext","ValidateContext method [Direct3D 11]","ValidateContext method [Direct3D 11]","ID3D11Debug interface","d3d11sdklayers/ID3D11Debug::ValidateContext","direct3d11.id3d11debug_validatecontext"]
old-location: direct3d11\id3d11debug_validatecontext.htm
tech.root: direct3d11
ms.assetid: c8679a68-336f-4bfa-91d6-398a75b34dfb
ms.date: 12/05/2018
ms.keywords: 4ee713bf-94e0-0a30-fb72-d6e8a2216e88, ID3D11Debug interface [Direct3D 11],ValidateContext method, ID3D11Debug.ValidateContext, ID3D11Debug::ValidateContext, ValidateContext, ValidateContext method [Direct3D 11], ValidateContext method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::ValidateContext, direct3d11.id3d11debug_validatecontext
req.header: d3d11sdklayers.h
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
 - ID3D11Debug::ValidateContext
 - d3d11sdklayers/ID3D11Debug::ValidateContext
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
 - ID3D11Debug.ValidateContext
---

# ID3D11Debug::ValidateContext


## -description

Check to see if the draw pipeline state is valid.

## -parameters

### -param pContext [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>, that represents a device context.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

Use validate prior to calling a draw method (for example, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-draw">ID3D11DeviceContext::Draw</a>); validation requires the debug layer.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11debug">ID3D11Debug Interface</a>