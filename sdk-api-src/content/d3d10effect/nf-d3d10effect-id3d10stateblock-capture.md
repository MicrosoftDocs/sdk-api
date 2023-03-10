---
UID: NF:d3d10effect.ID3D10StateBlock.Capture
title: ID3D10StateBlock::Capture (d3d10effect.h)
description: Capture the current value of states that are included in a stateblock. (ID3D10StateBlock.Capture)
helpviewer_keywords: ["9484ba4e-87ec-bd46-89ed-f4dc19c3d6e2","Capture","Capture method [Direct3D 10]","Capture method [Direct3D 10]","ID3D10StateBlock interface","ID3D10StateBlock interface [Direct3D 10]","Capture method","ID3D10StateBlock.Capture","ID3D10StateBlock::Capture","d3d10effect/ID3D10StateBlock::Capture","direct3d10.id3d10stateblock_capture"]
old-location: direct3d10\id3d10stateblock_capture.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock_capture.htm
ms.date: 12/05/2018
ms.keywords: 9484ba4e-87ec-bd46-89ed-f4dc19c3d6e2, Capture, Capture method [Direct3D 10], Capture method [Direct3D 10],ID3D10StateBlock interface, ID3D10StateBlock interface [Direct3D 10],Capture method, ID3D10StateBlock.Capture, ID3D10StateBlock::Capture, d3d10effect/ID3D10StateBlock::Capture, direct3d10.id3d10stateblock_capture
req.header: d3d10effect.h
req.include-header: D3D10.h
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
 - ID3D10StateBlock::Capture
 - d3d10effect/ID3D10StateBlock::Capture
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
 - ID3D10StateBlock.Capture
---

# ID3D10StateBlock::Capture


## -description

Capture the current value of states that are included in a stateblock.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

Capture captures current values for states within an existing state block. It does not capture the entire state of the device. Creating an empty stateblock and calling Capture does nothing if no states have been set.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock">ID3D10StateBlock Interface</a>
