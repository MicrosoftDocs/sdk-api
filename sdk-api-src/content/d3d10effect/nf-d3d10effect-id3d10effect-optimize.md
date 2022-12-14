---
UID: NF:d3d10effect.ID3D10Effect.Optimize
title: ID3D10Effect::Optimize (d3d10effect.h)
description: Minimize the amount of memory required for an effect.
helpviewer_keywords: ["ID3D10Effect interface [Direct3D 10]","Optimize method","ID3D10Effect.Optimize","ID3D10Effect::Optimize","Optimize","Optimize method [Direct3D 10]","Optimize method [Direct3D 10]","ID3D10Effect interface","d3d10effect/ID3D10Effect::Optimize","direct3d10.id3d10effect_optimize","fbbf4573-f405-bce6-e72a-a861f2d82e60"]
old-location: direct3d10\id3d10effect_optimize.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_optimize.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Effect interface [Direct3D 10],Optimize method, ID3D10Effect.Optimize, ID3D10Effect::Optimize, Optimize, Optimize method [Direct3D 10], Optimize method [Direct3D 10],ID3D10Effect interface, d3d10effect/ID3D10Effect::Optimize, direct3d10.id3d10effect_optimize, fbbf4573-f405-bce6-e72a-a861f2d82e60
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
 - ID3D10Effect::Optimize
 - d3d10effect/ID3D10Effect::Optimize
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
 - ID3D10Effect.Optimize
---

# ID3D10Effect::Optimize


## -description

Minimize the amount of memory required for an effect.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata 
      required to reflect information back to an application using the API. You can minimize the amount of memory required by an effect by 
      calling <b>ID3D10Effect::Optimize</b> which removes the reflection metadata from memory. API methods to read variables will no 
      longer work once reflection data has been removed.

The following methods will fail after Optimize has been called on an effect.

<ul>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getconstantbufferbyindex">ID3D10Effect::GetConstantBufferByIndex</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getconstantbufferbyname">ID3D10Effect::GetConstantBufferByName</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getdesc">ID3D10Effect::GetDesc</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getdevice">ID3D10Effect::GetDevice</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-gettechniquebyindex">ID3D10Effect::GetTechniqueByIndex</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-gettechniquebyname">ID3D10Effect::GetTechniqueByName</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getvariablebyindex">ID3D10Effect::GetVariableByIndex</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getvariablebyname">ID3D10Effect::GetVariableByName</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getvariablebysemantic">ID3D10Effect::GetVariableBySemantic</a>
</li>
</ul>
Note that references retrieved with these methods before calling <b>ID3D10Effect::Optimize</b> are still valid 
      after <b>ID3D10Effect::Optimize</b> is called.  This allows the application to get all the variables, techniques, and passes it will use, 
      call Optimize, and then use the effect.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>
