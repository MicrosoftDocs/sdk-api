---
UID: NF:d3d12.ID3D12GraphicsCommandList.IASetPrimitiveTopology
title: ID3D12GraphicsCommandList::IASetPrimitiveTopology (d3d12.h)
description: Bind information about the primitive type, and data order that describes input data for the input assembler stage. (ID3D12GraphicsCommandList.IASetPrimitiveTopology)
helpviewer_keywords: ["IASetPrimitiveTopology","IASetPrimitiveTopology method","IASetPrimitiveTopology method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","IASetPrimitiveTopology method","ID3D12GraphicsCommandList.IASetPrimitiveTopology","ID3D12GraphicsCommandList::IASetPrimitiveTopology","d3d12/ID3D12GraphicsCommandList::IASetPrimitiveTopology","direct3d12.id3d12graphicscommandlist_iasetprimitivetopology"]
old-location: direct3d12\id3d12graphicscommandlist_iasetprimitivetopology.htm
tech.root: direct3d12
ms.assetid: 743C48DF-C67E-48A0-B027-B2776E65968F
ms.date: 12/05/2018
ms.keywords: IASetPrimitiveTopology, IASetPrimitiveTopology method, IASetPrimitiveTopology method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,IASetPrimitiveTopology method, ID3D12GraphicsCommandList.IASetPrimitiveTopology, ID3D12GraphicsCommandList::IASetPrimitiveTopology, d3d12/ID3D12GraphicsCommandList::IASetPrimitiveTopology, direct3d12.id3d12graphicscommandlist_iasetprimitivetopology
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::IASetPrimitiveTopology
 - d3d12/ID3D12GraphicsCommandList::IASetPrimitiveTopology
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.IASetPrimitiveTopology
---

# ID3D12GraphicsCommandList::IASetPrimitiveTopology


## -description

Bind information about the primitive type, and data order that describes input data for the input assembler stage.

## -parameters

### -param PrimitiveTopology [in]

Type: <b>D3D12_PRIMITIVE_TOPOLOGY</b>

The type of primitive and ordering of the primitive data (see <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology">D3D_PRIMITIVE_TOPOLOGY</a>).

## -see-also

<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type">D3D12_PRIMITIVE_TOPOLOGY_TYPE</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
