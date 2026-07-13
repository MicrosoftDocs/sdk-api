---
UID: NE:d3d12.D3D12_WRITEBUFFERIMMEDIATE_MODE
title: D3D12_WRITEBUFFERIMMEDIATE_MODE (d3d12.h)
description: Specifies the mode used by a WriteBufferImmediate operation.
helpviewer_keywords: ["D3D12_WRITEBUFFERIMMEDIATE_MODE","D3D12_WRITEBUFFERIMMEDIATE_MODE enumeration","D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT","D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN","D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT","d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE","d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT","d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN","d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT","direct3d12.d3d12_writebufferimmediate_mode"]
old-location: direct3d12\d3d12_writebufferimmediate_mode.htm
tech.root: direct3d12
ms.assetid: 0AB6674C-B73E-4C38-8B6F-18B9BE596B71
ms.date: 12/05/2018
ms.keywords: D3D12_WRITEBUFFERIMMEDIATE_MODE, D3D12_WRITEBUFFERIMMEDIATE_MODE enumeration, D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT, D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN, D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT, d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE, d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT, d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN, d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT, direct3d12.d3d12_writebufferimmediate_mode
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_WRITEBUFFERIMMEDIATE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_WRITEBUFFERIMMEDIATE_MODE
 - d3d12/D3D12_WRITEBUFFERIMMEDIATE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_WRITEBUFFERIMMEDIATE_MODE
---

# D3D12_WRITEBUFFERIMMEDIATE_MODE enumeration


## -description

Specifies the mode used by a <b>WriteBufferImmediate</b> operation.

## -enum-fields

### -field D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT:0

The write operation behaves the same as normal copy-write operations.

### -field D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN:0x1

The write operation is guaranteed to occur after all preceding commands in the command stream have started, including previous <b>WriteBufferImmediate</b> operations.

### -field D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT:0x2

The write operation is deferred until all previous commands in the command stream have completed through the GPU pipeline, including previous <b>WriteBufferImmediate</b> operations. Write operations that specify <b>D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT</b> don't block subsequent operations from starting. If there are no previous operations in the command stream, then the write operation behaves as if <b>D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN</b> was specified.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist2">ID3D12GraphicsCommandList::WriteBufferImmediate</a>
