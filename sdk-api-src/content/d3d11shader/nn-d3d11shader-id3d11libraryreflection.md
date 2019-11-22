---
UID: NN:d3d11shader.ID3D11LibraryReflection
title: ID3D11LibraryReflection (d3d11shader.h)

description: A library-reflection interface accesses library info.
old-location: direct3d11\id3d11libraryreflection.htm
tech.root: direct3d11
ms.assetid: 59792EC6-B739-4D86-84F6-DC03AD3016F1

ms.date: 12/05/2018
ms.keywords: ID3D11LibraryReflection, ID3D11LibraryReflection interface [Direct3D 11], ID3D11LibraryReflection interface [Direct3D 11],described, d3d11shader/ID3D11LibraryReflection, direct3d11.id3d11libraryreflection
ms.topic: interface
f1_keywords: 
 - "d3d11shader/ID3D11LibraryReflection"
dev_langs:
 - c++
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11LibraryReflection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11LibraryReflection interface


## -description


A library-reflection interface accesses library info. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11LibraryReflection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11LibraryReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11LibraryReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11libraryreflection-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Fills the library descriptor structure for the library reflection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11libraryreflection-getfunctionbyindex">GetFunctionByIndex</a>
</td>
<td align="left" width="63%">
Gets the function reflector.

</td>
</tr>
</table> 


## -remarks



To get a library-reflection interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dreflectlibrary">D3DReflectLibrary</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11LibraryReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

