---
UID: NF:d3d10.ID3D10Device.IASetPrimitiveTopology
title: ID3D10Device::IASetPrimitiveTopology (d3d10.h)
description: Bind information about the primitive type, and data order that describes input data for the input assembler stage. (ID3D10Device.IASetPrimitiveTopology)
helpviewer_keywords: ["574e830c-3db9-ca52-4b41-1b3e8224137a","IASetPrimitiveTopology","IASetPrimitiveTopology method [Direct3D 10]","IASetPrimitiveTopology method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","IASetPrimitiveTopology method","ID3D10Device.IASetPrimitiveTopology","ID3D10Device::IASetPrimitiveTopology","d3d10/ID3D10Device::IASetPrimitiveTopology","direct3d10.id3d10device_iasetprimitivetopology"]
old-location: direct3d10\id3d10device_iasetprimitivetopology.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetprimitivetopology.htm
ms.date: 12/05/2018
ms.keywords: 574e830c-3db9-ca52-4b41-1b3e8224137a, IASetPrimitiveTopology, IASetPrimitiveTopology method [Direct3D 10], IASetPrimitiveTopology method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetPrimitiveTopology method, ID3D10Device.IASetPrimitiveTopology, ID3D10Device::IASetPrimitiveTopology, d3d10/ID3D10Device::IASetPrimitiveTopology, direct3d10.id3d10device_iasetprimitivetopology
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
 - ID3D10Device::IASetPrimitiveTopology
 - d3d10/ID3D10Device::IASetPrimitiveTopology
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
 - ID3D10Device.IASetPrimitiveTopology
---

# ID3D10Device::IASetPrimitiveTopology


## -description

Bind information about the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies">primitive type</a>, and data order that describes input data for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input assembler</a> stage.

## -parameters

### -param Topology [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb205334(v=vs.85)">D3D10_PRIMITIVE_TOPOLOGY</a></b>

The type of primitive and ordering of the primitive data (see <a href="/previous-versions/windows/desktop/legacy/bb205334(v=vs.85)">D3D10_PRIMITIVE_TOPOLOGY</a>).

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
