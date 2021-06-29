---
UID: NF:d3d10effect.ID3D10Effect.IsOptimized
title: ID3D10Effect::IsOptimized (d3d10effect.h)
description: Test an effect to see if the reflection metadata has been removed from memory.
helpviewer_keywords: ["0d82fdb1-e0b0-7198-dd16-2dfcd0280bfe","ID3D10Effect interface [Direct3D 10]","IsOptimized method","ID3D10Effect.IsOptimized","ID3D10Effect::IsOptimized","IsOptimized","IsOptimized method [Direct3D 10]","IsOptimized method [Direct3D 10]","ID3D10Effect interface","d3d10effect/ID3D10Effect::IsOptimized","direct3d10.id3d10effect_isoptimized"]
old-location: direct3d10\id3d10effect_isoptimized.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_isoptimized.htm
ms.date: 12/05/2018
ms.keywords: 0d82fdb1-e0b0-7198-dd16-2dfcd0280bfe, ID3D10Effect interface [Direct3D 10],IsOptimized method, ID3D10Effect.IsOptimized, ID3D10Effect::IsOptimized, IsOptimized, IsOptimized method [Direct3D 10], IsOptimized method [Direct3D 10],ID3D10Effect interface, d3d10effect/ID3D10Effect::IsOptimized, direct3d10.id3d10effect_isoptimized
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Effect::IsOptimized
 - d3d10effect/ID3D10Effect::IsOptimized
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10Effect.IsOptimized
---

# ID3D10Effect::IsOptimized


## -description

Test an effect to see if the reflection metadata has been removed from memory.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the effect is optimized; otherwise <b>FALSE</b>.

## -remarks

An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API. You can minimize the amount of memory required by an effect by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-optimize">ID3D10Effect::Optimize</a> which removes the reflection metadata from memory. Of course, API methods to read variables will no longer work once reflection data has been removed.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>
