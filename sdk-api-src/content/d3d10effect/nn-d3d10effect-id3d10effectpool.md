---
UID: NN:d3d10effect.ID3D10EffectPool
title: ID3D10EffectPool (d3d10effect.h)
description: A pool interface represents a common memory space (or pool) for sharing variables between effects.
helpviewer_keywords: ["3c4865e5-4958-111b-ced6-75e2e367d986","ID3D10EffectPool","ID3D10EffectPool interface [Direct3D 10]","ID3D10EffectPool interface [Direct3D 10]","described","d3d10effect/ID3D10EffectPool","direct3d10.id3d10effectpool"]
old-location: direct3d10\id3d10effectpool.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpool.htm
ms.date: 12/05/2018
ms.keywords: 3c4865e5-4958-111b-ced6-75e2e367d986, ID3D10EffectPool, ID3D10EffectPool interface [Direct3D 10], ID3D10EffectPool interface [Direct3D 10],described, d3d10effect/ID3D10EffectPool, direct3d10.id3d10effectpool
req.header: d3d10effect.h
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
 - ID3D10EffectPool
 - d3d10effect/ID3D10EffectPool
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
 - ID3D10EffectPool
---

# ID3D10EffectPool interface


## -description

A pool interface represents a common memory space (or pool) for sharing variables between effects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectPool</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10EffectPool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectPool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpool-aseffect">AsEffect</a>
</td>
<td align="left" width="63%">
Get the effect that created the effect pool.

</td>
</tr>
</table>

## -remarks

To create an effect pool, call a function like <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3dx10createeffectpoolfromfile">D3DX10CreateEffectPoolFromFile</a>. Effect pools can improve performance by reducing the number of API calls required to make state changes (see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-performance">Using Effect Pools</a>).

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>

