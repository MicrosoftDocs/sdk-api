---
UID: NF:d3d10effect.D3D10CreateEffectFromMemory
title: D3D10CreateEffectFromMemory function (d3d10effect.h)
description: Creates an ID3D10Effect from a buffer containing a compiled effect.helpviewer_keywords: ["D3D10CreateEffectFromMemory","D3D10CreateEffectFromMemory function [Direct3D 10]","d3d10effect/D3D10CreateEffectFromMemory","direct3d10.d3d10createeffectfrommemory","f306b99a-20d9-c501-65b4-81dd11930f56"]
old-location: direct3d10\d3d10createeffectfrommemory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createeffectfrommemory.htm
ms.date: 12/05/2018
ms.keywords: D3D10CreateEffectFromMemory, D3D10CreateEffectFromMemory function [Direct3D 10], d3d10effect/D3D10CreateEffectFromMemory, direct3d10.d3d10createeffectfrommemory, f306b99a-20d9-c501-65b4-81dd11930f56
f1_keywords:
- d3d10effect/D3D10CreateEffectFromMemory
dev_langs:
- c++
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
req.dll: D3D10.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- D3D10.dll
api_name:
- D3D10CreateEffectFromMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3D10CreateEffectFromMemory function


## -description


Creates an ID3D10Effect from a buffer containing a compiled effect.


## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to a compiled effect.


### -param DataLength [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pData</i>.


### -param FXFlags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Effect <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants">compile options</a>.


### -param pDevice [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>*</b>

A pointer to the device (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>).


### -param pEffectPool [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpool">ID3D10EffectPool</a>*</b>

Optional. A pointer to an memory space for effect variables that are shared across effects (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpool">ID3D10EffectPool Interface</a>).


### -param ppEffect [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a>**</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a> which contains the created effect.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



This method is used to create an <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a> object from an effect that has been compiled before runtime and loaded into memory.  
      For help precompiling an effect, see <a href="https://docs.microsoft.com/windows/desktop/direct3dtools/dx-graphics-tools-fxc-using">Offline Compiling</a>.  
      To load and compile an ASCII .fx file see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-compile">Compile an Effect (Direct3D 10)</a>.


#### Examples

Compiling and loading an effect
          

Compile the effect.


```

fxc.exe /T fx_4_0 /Fo Tutorial03.fxo Tutorial03.fx      
          
```


Load the compiled effect at runtime.


```

ifstream is("tutorial03.fxo", ios::binary);
is.seekg(0,ios_base::end);
streampos pos = is.tellg();
is.seekg(0,ios_base::beg);
char * effectBuffer = new char[pos];
is.read(effectBuffer,pos);
	
hr = D3D10CreateEffectFromMemory((void *)effectBuffer,pos,0,g_pd3dDevice,NULL,&g_pEffect);
          
```


<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions (Direct3D 10)</a>
 

 

