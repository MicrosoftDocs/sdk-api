---
UID: NN:d3d12shader.ID3D12LibraryReflection
title: ID3D12LibraryReflection (d3d12shader.h)
description: A library-reflection interface accesses library info.
old-location: direct3d12\id3d12libraryreflection.htm
tech.root: direct3d12
ms.assetid: CE6AEA77-A6A0-46A5-BDBC-AE4907AAC820
ms.date: 12/05/2018
ms.keywords: ID3D12LibraryReflection, ID3D12LibraryReflection interface, ID3D12LibraryReflection interface,described, d3d12shader/ID3D12LibraryReflection, direct3d12.id3d12libraryreflection
ms.topic: interface
f1_keywords:
- d3d12shader/ID3D12LibraryReflection
dev_langs:
- c++
req.header: d3d12shader.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12shader.h
api_name:
- ID3D12LibraryReflection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12LibraryReflection interface


## -description


A library-reflection interface accesses library info.
          <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12LibraryReflection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12LibraryReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12LibraryReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12libraryreflection-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Fills the library descriptor structure for the library reflection.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12libraryreflection-getfunctionbyindex">GetFunctionByIndex</a>
</td>
<td align="left" width="63%">
Gets the function reflector.
        

</td>
</tr>
</table> 


## -remarks



To get a library-reflection interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dreflectlibrary">D3DReflectLibrary</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D12LibraryReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
 

 

