---
UID: NS:d3d12.D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
title: D3D12_WRITEBUFFERIMMEDIATE_PARAMETER (d3d12.h)
description: Specifies the immediate value and destination address written using ID3D12CommandList2::WriteBufferImmediate.
helpviewer_keywords: ["D3D12_WRITEBUFFERIMMEDIATE_PARAMETER","D3D12_WRITEBUFFERIMMEDIATE_PARAMETER structure","d3d12/D3D12_WRITEBUFFERIMMEDIATE_PARAMETER","direct3d12.d3d12_writebufferimmediate_parameter"]
old-location: direct3d12\d3d12_writebufferimmediate_parameter.htm
tech.root: direct3d12
ms.assetid: 7CF8A888-BB3A-4557-8DA5-7AFAFC6747CF
ms.date: 12/05/2018
ms.keywords: D3D12_WRITEBUFFERIMMEDIATE_PARAMETER, D3D12_WRITEBUFFERIMMEDIATE_PARAMETER structure, d3d12/D3D12_WRITEBUFFERIMMEDIATE_PARAMETER, direct3d12.d3d12_writebufferimmediate_parameter
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
req.typenames: D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
 - d3d12/D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
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
 - D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
---

# D3D12_WRITEBUFFERIMMEDIATE_PARAMETER structure


## -description

Specifies the immediate value and destination address written using <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate">ID3D12GraphicsCommandList2::WriteBufferImmediate</a>.

## -struct-fields

### -field Dest

The GPU virtual address at which to write the value. The address must be aligned to a 32-bit (4-byte) boundary.

### -field Value

The 32-bit value to write.

## -remarks

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
