---
UID: NF:d3d12.ID3D12GraphicsCommandList2.WriteBufferImmediate
title: ID3D12GraphicsCommandList2::WriteBufferImmediate (d3d12.h)
description: Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream. (ID3D12GraphicsCommandList2.WriteBufferImmediate)
helpviewer_keywords: ["ID3D12GraphicsCommandList2 interface","WriteBufferImmediate method","ID3D12GraphicsCommandList2.WriteBufferImmediate","ID3D12GraphicsCommandList2::WriteBufferImmediate","WriteBufferImmediate","WriteBufferImmediate method","WriteBufferImmediate method","ID3D12GraphicsCommandList2 interface","d3d12/ID3D12GraphicsCommandList2::WriteBufferImmediate","direct3d12.id3d12graphicscommandlist2_writebufferimmediate_uint_parameter_mode"]
old-location: direct3d12\id3d12graphicscommandlist2_writebufferimmediate_uint_parameter_mode.htm
tech.root: direct3d12
ms.assetid: EB1FD3E0-5785-40D1-961B-AF22F9911653
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList2 interface,WriteBufferImmediate method, ID3D12GraphicsCommandList2.WriteBufferImmediate, ID3D12GraphicsCommandList2::WriteBufferImmediate, WriteBufferImmediate, WriteBufferImmediate method, WriteBufferImmediate method,ID3D12GraphicsCommandList2 interface, d3d12/ID3D12GraphicsCommandList2::WriteBufferImmediate, direct3d12.id3d12graphicscommandlist2_writebufferimmediate_uint_parameter_mode
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList2::WriteBufferImmediate
 - d3d12/ID3D12GraphicsCommandList2::WriteBufferImmediate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList2.WriteBufferImmediate
---

# ID3D12GraphicsCommandList2::WriteBufferImmediate


## -description

Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream.

## -parameters

### -param Count

The number of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter">D3D12_WRITEBUFFERIMMEDIATE_PARAMETER</a> structures that are pointed to by <i>pParams</i> and <i>pModes</i>.

### -param pParams [in]

The address of an array containing a number of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter">D3D12_WRITEBUFFERIMMEDIATE_PARAMETER</a> structures equal to <i>Count</i>.

### -param pModes [in, optional]

The address of an array containing a number of  <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode">D3D12_WRITEBUFFERIMMEDIATE_MODE</a> structures equal to <i>Count</i>. The default value is <b>null</b>; passing <b>null</b> causes the system to write all immediate values using <b>D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT</b>.

## -remarks

<b>WriteBufferImmediate</b> performs <i>Count</i> number of 32-bit writes: one for each value and destination specified in <i>pParams</i>.

The receiving buffer (resource) must be in the <b>D3D12_RESOURCE_STATE_COPY_DEST</b> state to be a valid destination for <b>WriteBufferImmediate</b>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist2">ID3D12GraphicsCommandList2</a>
