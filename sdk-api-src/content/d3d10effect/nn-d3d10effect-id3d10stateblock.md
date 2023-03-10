---
UID: NN:d3d10effect.ID3D10StateBlock
title: ID3D10StateBlock (d3d10effect.h)
description: A state-block interface encapsulates render states.
helpviewer_keywords: ["23872e09-b63b-11d0-bb95-f57009f0fab6","ID3D10StateBlock","ID3D10StateBlock interface [Direct3D 10]","ID3D10StateBlock interface [Direct3D 10]","described","d3d10effect/ID3D10StateBlock","direct3d10.id3d10stateblock"]
old-location: direct3d10\id3d10stateblock.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock.htm
ms.date: 12/05/2018
ms.keywords: 23872e09-b63b-11d0-bb95-f57009f0fab6, ID3D10StateBlock, ID3D10StateBlock interface [Direct3D 10], ID3D10StateBlock interface [Direct3D 10],described, d3d10effect/ID3D10StateBlock, direct3d10.id3d10stateblock
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
 - ID3D10StateBlock
 - d3d10effect/ID3D10StateBlock
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
 - ID3D10StateBlock
---

# ID3D10StateBlock interface


## -description

A state-block interface encapsulates render states.

## -inheritance

The <b>ID3D10StateBlock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10StateBlock</b> also has these types of members:

## -remarks

To create a state-block interface, call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-d3d10createstateblock">D3D10CreateStateBlock</a>.

This interface can be used to save and restore pipeline state. It can also be used to capture the current state.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
