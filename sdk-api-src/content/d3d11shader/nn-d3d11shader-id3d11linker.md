---
UID: NN:d3d11shader.ID3D11Linker
title: ID3D11Linker (d3d11shader.h)
description: A linker interface is used to link a shader module.
old-location: direct3d11\id3d11linker.htm
tech.root: direct3d11
ms.assetid: 08967A5F-AAAE-4352-A8A9-C7B1ED16EF25
ms.date: 12/05/2018
ms.keywords: ID3D11Linker, ID3D11Linker interface [Direct3D 11], ID3D11Linker interface [Direct3D 11],described, d3d11shader/ID3D11Linker, direct3d11.id3d11linker
f1_keywords:
- d3d11shader/ID3D11Linker
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
- ID3D11Linker
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Linker interface


## -description


A linker interface is used to link a shader module. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Linker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Linker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Linker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-addclipplanefromcbuffer">AddClipPlaneFromCBuffer</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9">clip plane</a> with the plane coefficients taken from a <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-constants">cbuffer</a> entry for 10Level9 shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link">Link</a>
</td>
<td align="left" width="63%">
Links the shader and produces a shader blob that the Direct3D runtime can use.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary">UseLibrary</a>
</td>
<td align="left" width="63%">
Adds an instance of a library module to be used for linking.

</td>
</tr>
</table> 


## -remarks



To get a linker interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dcreatelinker">D3DCreateLinker</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11Linker</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

