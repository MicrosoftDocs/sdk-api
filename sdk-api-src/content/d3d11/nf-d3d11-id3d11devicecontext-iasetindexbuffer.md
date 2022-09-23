---
UID: NF:d3d11.ID3D11DeviceContext.IASetIndexBuffer
title: ID3D11DeviceContext::IASetIndexBuffer (d3d11.h)
description: Bind an index buffer to the input-assembler stage. (ID3D11DeviceContext.IASetIndexBuffer)
helpviewer_keywords: ["73896724-c6e5-3a60-25c3-af31308264c5","IASetIndexBuffer","IASetIndexBuffer method [Direct3D 11]","IASetIndexBuffer method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","IASetIndexBuffer method","ID3D11DeviceContext.IASetIndexBuffer","ID3D11DeviceContext::IASetIndexBuffer","d3d11/ID3D11DeviceContext::IASetIndexBuffer","direct3d11.id3d11devicecontext_iasetindexbuffer"]
old-location: direct3d11\id3d11devicecontext_iasetindexbuffer.htm
tech.root: direct3d11
ms.assetid: c556dda2-0808-4701-90cb-16c67a24add1
ms.date: 12/05/2018
ms.keywords: 73896724-c6e5-3a60-25c3-af31308264c5, IASetIndexBuffer, IASetIndexBuffer method [Direct3D 11], IASetIndexBuffer method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IASetIndexBuffer method, ID3D11DeviceContext.IASetIndexBuffer, ID3D11DeviceContext::IASetIndexBuffer, d3d11/ID3D11DeviceContext::IASetIndexBuffer, direct3d11.id3d11devicecontext_iasetindexbuffer
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
 - ID3D11DeviceContext::IASetIndexBuffer
 - d3d11/ID3D11DeviceContext::IASetIndexBuffer
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
 - ID3D11DeviceContext.IASetIndexBuffer
---

# ID3D11DeviceContext::IASetIndexBuffer


## -description

Bind an index buffer to the input-assembler stage.

## -parameters

### -param pIndexBuffer [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> object, that contains indices. The index buffer must have been created with
            the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_INDEX_BUFFER</a> flag.

### -param Format [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> that specifies the format of the data in the index buffer. The only formats allowed for index
            buffer data are 16-bit (DXGI_FORMAT_R16_UINT) and 32-bit (DXGI_FORMAT_R32_UINT) integers.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset (in bytes) from the start of the index buffer to the first index to use.

## -remarks

For information about creating index buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to">How to: Create an Index Buffer</a>.
        

Calling this method using a buffer that is currently bound for writing (i.e. bound to the stream output pipeline stage) will effectively bind
          <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.
        

The debug layer will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will
          not prevent invalid data from being used by the runtime.
        

The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
