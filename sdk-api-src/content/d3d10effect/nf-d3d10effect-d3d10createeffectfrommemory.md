---
UID: NF:d3d10effect.D3D10CreateEffectFromMemory
title: D3D10CreateEffectFromMemory function (d3d10effect.h)
description: Creates an ID3D10Effect from a buffer containing a compiled effect.
helpviewer_keywords: ["D3D10CreateEffectFromMemory","D3D10CreateEffectFromMemory function [Direct3D 10]","d3d10effect/D3D10CreateEffectFromMemory","direct3d10.d3d10createeffectfrommemory","f306b99a-20d9-c501-65b4-81dd11930f56"]
old-location: direct3d10\d3d10createeffectfrommemory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createeffectfrommemory.htm
ms.date: 05/16/2023
ms.keywords: D3D10CreateEffectFromMemory, D3D10CreateEffectFromMemory function [Direct3D 10], d3d10effect/D3D10CreateEffectFromMemory, direct3d10.d3d10createeffectfrommemory, f306b99a-20d9-c501-65b4-81dd11930f56
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
 - D3D10CreateEffectFromMemory
 - d3d10effect/D3D10CreateEffectFromMemory
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
 - D3D10CreateEffectFromMemory
---

## -description

Creates an ID3D10Effect from a buffer containing a compiled effect.

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

### -param pEffectPool [in]

Type: <b><a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effectpool">ID3D10EffectPool</a>*</b>

Optional. A pointer to a memory space for effect variables that are shared across effects (see <a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effectpool">ID3D10EffectPool Interface</a>).

### -param ppEffect [out]

Type: <b><a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a>**</b>

A pointer to an <a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a> which contains the created effect.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/win32/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

> [!NOTE]
> Linking `d3d10_1.lib` gives you the implementation in `d3d10_1.dll`, which is the Direct3D10.1 programming model implementation. Linking `d3d10.lib` gives you the implementation in `d3d10.dll`, which is the Direct3D10 programming model implementation.

This method is used to create an <a href="/windows/win32/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a> object from an effect that has been compiled before runtime and loaded into memory. For help precompiling an effect, see <a href="/windows/win32/direct3dtools/dx-graphics-tools-fxc-using">Offline Compiling</a>. To load and compile an ASCII .fx file see <a href="/windows/win32/direct3d10/d3d10-graphics-programming-guide-effects-compile">Compile an Effect (Direct3D 10)</a>.

## Examples

### Compile the effect

```
fxc.exe /T fx_4_0 /Fo Tutorial03.fxo Tutorial03.fx      
```

### Load the compiled effect at runtime.

```
ifstream is("tutorial03.fxo", ios::binary);
is.seekg(0,ios_base::end);
streampos pos = is.tellg();
is.seekg(0,ios_base::beg);
char * effectBuffer = new char[pos];
is.read(effectBuffer,pos);
	
hr = D3D10CreateEffectFromMemory((void *)effectBuffer,pos,0,g_pd3dDevice,NULL,&g_pEffect);
```

## -see-also

<a href="/windows/win32/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions (Direct3D 10)</a>
