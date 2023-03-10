---
UID: NF:d3d11.ID3D11DeviceContext.DrawIndexed
title: ID3D11DeviceContext::DrawIndexed (d3d11.h)
description: Draw indexed, non-instanced primitives. (ID3D11DeviceContext.DrawIndexed)
helpviewer_keywords: ["45129747-420c-37ba-aae0-05275af46932","DrawIndexed","DrawIndexed method [Direct3D 11]","DrawIndexed method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DrawIndexed method","ID3D11DeviceContext.DrawIndexed","ID3D11DeviceContext::DrawIndexed","d3d11/ID3D11DeviceContext::DrawIndexed","direct3d11.id3d11devicecontext_drawindexed"]
old-location: direct3d11\id3d11devicecontext_drawindexed.htm
tech.root: direct3d11
ms.assetid: 461a64ec-f3e6-4f6a-8bc4-a349d19501a8
ms.date: 12/05/2018
ms.keywords: 45129747-420c-37ba-aae0-05275af46932, DrawIndexed, DrawIndexed method [Direct3D 11], DrawIndexed method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawIndexed method, ID3D11DeviceContext.DrawIndexed, ID3D11DeviceContext::DrawIndexed, d3d11/ID3D11DeviceContext::DrawIndexed, direct3d11.id3d11devicecontext_drawindexed
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
 - ID3D11DeviceContext::DrawIndexed
 - d3d11/ID3D11DeviceContext::DrawIndexed
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
 - ID3D11DeviceContext.DrawIndexed
---

# ID3D11DeviceContext::DrawIndexed


## -description

Draw indexed, non-instanced primitives.

## -parameters

### -param IndexCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of indices to draw.

### -param StartIndexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The location of the first index read by the GPU from the index buffer.

### -param BaseVertexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value added to each index before reading a vertex from the vertex buffer.

## -remarks

A draw API submits work to the rendering pipeline.

If the sum of both indices is negative, the result of the function call is undefined.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
