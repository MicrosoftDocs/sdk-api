---
UID: NF:d3d10.ID3D10Device.IASetIndexBuffer
title: ID3D10Device::IASetIndexBuffer (d3d10.h)
description: Bind an index buffer to the input-assembler stage. (ID3D10Device.IASetIndexBuffer)
helpviewer_keywords: ["608d16ec-f6d6-ea93-bc37-fe7d34d07215","IASetIndexBuffer","IASetIndexBuffer method [Direct3D 10]","IASetIndexBuffer method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","IASetIndexBuffer method","ID3D10Device.IASetIndexBuffer","ID3D10Device::IASetIndexBuffer","d3d10/ID3D10Device::IASetIndexBuffer","direct3d10.id3d10device_iasetindexbuffer"]
old-location: direct3d10\id3d10device_iasetindexbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetindexbuffer.htm
ms.date: 12/05/2018
ms.keywords: 608d16ec-f6d6-ea93-bc37-fe7d34d07215, IASetIndexBuffer, IASetIndexBuffer method [Direct3D 10], IASetIndexBuffer method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetIndexBuffer method, ID3D10Device.IASetIndexBuffer, ID3D10Device::IASetIndexBuffer, d3d10/ID3D10Device::IASetIndexBuffer, direct3d10.id3d10device_iasetindexbuffer
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
 - ID3D10Device::IASetIndexBuffer
 - d3d10/ID3D10Device::IASetIndexBuffer
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
 - ID3D10Device.IASetIndexBuffer
---

# ID3D10Device::IASetIndexBuffer


## -description

Bind an <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">index buffer</a> to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage.

## -parameters

### -param pIndexBuffer [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>*</b>

A pointer to a buffer (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>) that contains indices. The index buffer must have been created with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_INDEX_BUFFER</a> flag.

### -param Format [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

Specifies format of the data in the index buffer. The only formats allowed for index buffer data are 16-bit (<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R16_UINT</a>) and 32-bit (<b>DXGI_FORMAT_R32_UINT</b>) integers.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset (in bytes) from the start of the index buffer to the first index to use.

## -remarks

For information about creating index buffers, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating">Create an Index Buffer</a>.

Calling this method using a buffer that is currently bound for writing (i.e. bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">stream output</a> pipeline stage) will effectively bind <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.

The <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">Debug Layer</a> will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
