---
UID: NN:d3d11shader.ID3D11LibraryReflection
title: ID3D11LibraryReflection (d3d11shader.h)
author: windows-sdk-content
description: A library-reflection interface accesses library info.
old-location: direct3d11\id3d11libraryreflection.htm
tech.root: direct3d11
ms.assetid: 59792EC6-B739-4D86-84F6-DC03AD3016F1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11LibraryReflection, ID3D11LibraryReflection interface [Direct3D 11], ID3D11LibraryReflection interface [Direct3D 11],described, d3d11shader/ID3D11LibraryReflection, direct3d11.id3d11libraryreflection
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11LibraryReflection interface


## -description


A library-reflection interface accesses library info. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11LibraryReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11LibraryReflection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/F23FEED8-94A3-4A87-8B4F-1D55BD47AF5F">GetDesc</a>
</td>
<td align="left" width="63%">
Fills the library descriptor structure for the library reflection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3058CCB5-E58E-4EEC-AEB9-C47B78DD6E79">GetFunctionByIndex</a>
</td>
<td align="left" width="63%">
Gets the function reflector.

</td>
</tr>
</table> 


## -remarks



To get a library-reflection interface, call <a href="https://msdn.microsoft.com/E64FB2C3-8F64-411F-89E1-984DAAE4D7C2">D3DReflectLibrary</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11LibraryReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

