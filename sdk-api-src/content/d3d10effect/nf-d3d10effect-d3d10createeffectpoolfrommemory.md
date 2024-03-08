---
UID: NF:d3d10effect.D3D10CreateEffectPoolFromMemory
title: D3D10CreateEffectPoolFromMemory function (d3d10effect.h)
description: Create an effect pool (or shared memory location), to enable sharing variables between effects.
helpviewer_keywords: ["D3D10CreateEffectPoolFromMemory","D3D10CreateEffectPoolFromMemory function [Direct3D 10]","d3d10effect/D3D10CreateEffectPoolFromMemory","direct3d10.d3d10createeffectpoolfrommemory","fe38c43e-d460-f70d-5972-0c60fb75b532"]
old-location: direct3d10\d3d10createeffectpoolfrommemory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createeffectpoolfrommemory.htm
ms.date: 05/16/2023
ms.keywords: D3D10CreateEffectPoolFromMemory, D3D10CreateEffectPoolFromMemory function [Direct3D 10], d3d10effect/D3D10CreateEffectPoolFromMemory, direct3d10.d3d10createeffectpoolfrommemory, fe38c43e-d460-f70d-5972-0c60fb75b532
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
req.lib: d3d10_1.lib, d3d10.lib
req.dll: d3d10_1.dll, d3d10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10CreateEffectPoolFromMemory
 - d3d10effect/D3D10CreateEffectPoolFromMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d10.dll
 - d3d10_1.dll
api_name:
 - D3D10CreateEffectPoolFromMemory
---

## -description

Create an effect pool (or shared memory location), to enable sharing variables between effects.

## -parameters

### -param pData [in]

Type: <b>void*</b>

A pointer to a compiled effect.

### -param DataLength [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pData</i>.

### -param FXFlags [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

Effect <a href="/windows/win32/direct3d10/d3d10-graphics-reference-effect-constants">compile options</a>.

### -param pDevice [in]

Type: <b><a href="/windows/win32/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>*</b>

A pointer to the device (see <a href="/windows/win32/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>).

### -param ppEffectPool [out]

Type: <b><a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effectpool">ID3D10EffectPool</a>**</b>

A pointer to the <a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effectpool">ID3D10EffectPool Interface</a> that contains the effect pool.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/win32/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

> [!NOTE]
> Linking `d3d10_1.lib` gives you the implementation in `d3d10_1.dll`, which is the Direct3D10.1 programming model implementation. Linking `d3d10.lib` gives you the implementation in `d3d10.dll`, which is the Direct3D10 programming model implementation.

A pool is a shared location in memory. Effect variables that are located in a pool can be updated once, and the effect system will take care of updating each effect that uses that variable. To pool an effect variable, tell the effect to locate the variable in a pool when the effect is created, using a helper function such as <a href="/windows/win32/direct3d10/d3dx10createeffectfromfile">D3DX10CreateEffectFromFile</a>.

For help compiling an effect, see <a href="/windows/win32/direct3d10/d3d10-graphics-programming-guide-effects-compile">Compile an Effect (Direct3D 10)</a>.

## -see-also

<a href="/windows/win32/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions (Direct3D 10)</a>
