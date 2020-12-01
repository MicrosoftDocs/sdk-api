---
UID: NF:d3d11sdklayers.ID3D11Debug.ValidateContextForDispatch
title: ID3D11Debug::ValidateContextForDispatch (d3d11sdklayers.h)
description: Verifies whether the dispatch pipeline state is valid.
helpviewer_keywords: ["ID3D11Debug interface [Direct3D 11]","ValidateContextForDispatch method","ID3D11Debug.ValidateContextForDispatch","ID3D11Debug::ValidateContextForDispatch","ValidateContextForDispatch","ValidateContextForDispatch method [Direct3D 11]","ValidateContextForDispatch method [Direct3D 11]","ID3D11Debug interface","d3d11sdklayers/ID3D11Debug::ValidateContextForDispatch","direct3d11.id3d11debug_validatecontextfordispatch"]
old-location: direct3d11\id3d11debug_validatecontextfordispatch.htm
tech.root: direct3d11
ms.assetid: 0ddabb4f-eeed-46d4-a1d2-501180edffe0
ms.date: 12/05/2018
ms.keywords: ID3D11Debug interface [Direct3D 11],ValidateContextForDispatch method, ID3D11Debug.ValidateContextForDispatch, ID3D11Debug::ValidateContextForDispatch, ValidateContextForDispatch, ValidateContextForDispatch method [Direct3D 11], ValidateContextForDispatch method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::ValidateContextForDispatch, direct3d11.id3d11debug_validatecontextfordispatch
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
 - ID3D11Debug::ValidateContextForDispatch
 - d3d11sdklayers/ID3D11Debug::ValidateContextForDispatch
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
 - ID3D11Debug.ValidateContextForDispatch
---

# ID3D11Debug::ValidateContextForDispatch


## -description

Verifies whether the dispatch pipeline state is valid.

## -parameters

### -param pContext [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> that represents a device context.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

Use this method before you call a dispatch method (for example, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">ID3D11DeviceContext::Dispatch</a>). Validation requires the debug layer.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11debug">ID3D11Debug</a>