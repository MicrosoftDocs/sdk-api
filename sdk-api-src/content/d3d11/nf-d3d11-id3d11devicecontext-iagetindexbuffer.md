---
UID: NF:d3d11.ID3D11DeviceContext.IAGetIndexBuffer
title: ID3D11DeviceContext::IAGetIndexBuffer (d3d11.h)
description: Get a pointer to the index buffer that is bound to the input-assembler stage. (ID3D11DeviceContext.IAGetIndexBuffer)
helpviewer_keywords: ["3fe40bcc-a76c-bfbf-97f0-0ee55d520b2d","IAGetIndexBuffer","IAGetIndexBuffer method [Direct3D 11]","IAGetIndexBuffer method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","IAGetIndexBuffer method","ID3D11DeviceContext.IAGetIndexBuffer","ID3D11DeviceContext::IAGetIndexBuffer","d3d11/ID3D11DeviceContext::IAGetIndexBuffer","direct3d11.id3d11devicecontext_iagetindexbuffer"]
old-location: direct3d11\id3d11devicecontext_iagetindexbuffer.htm
tech.root: direct3d11
ms.assetid: 948a5cbd-8413-4aaa-b666-7b9adc4705da
ms.date: 12/05/2018
ms.keywords: 3fe40bcc-a76c-bfbf-97f0-0ee55d520b2d, IAGetIndexBuffer, IAGetIndexBuffer method [Direct3D 11], IAGetIndexBuffer method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IAGetIndexBuffer method, ID3D11DeviceContext.IAGetIndexBuffer, ID3D11DeviceContext::IAGetIndexBuffer, d3d11/ID3D11DeviceContext::IAGetIndexBuffer, direct3d11.id3d11devicecontext_iagetindexbuffer
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
 - ID3D11DeviceContext::IAGetIndexBuffer
 - d3d11/ID3D11DeviceContext::IAGetIndexBuffer
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
 - ID3D11DeviceContext.IAGetIndexBuffer
---

# ID3D11DeviceContext::IAGetIndexBuffer


## -description

Get a pointer to the index buffer that is bound to the input-assembler stage.

## -parameters

### -param pIndexBuffer [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>**</b>

A pointer to an index buffer returned by the method (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>).

### -param Format [out, optional]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>*</b>

Specifies format of the data in the index buffer (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>). These formats provide the size and type of 
          the data in the buffer. The only formats allowed for index buffer data are 16-bit (DXGI_FORMAT_R16_UINT) and 32-bit (DXGI_FORMAT_R32_UINT) 
          integers.

### -param Offset [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Offset (in bytes) from the start of the index buffer, to the first index to use.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces 
      when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
