---
UID: NN:d3d11shader.ID3D11Linker
title: ID3D11Linker
author: windows-sdk-content
description: A linker interface is used to link a shader module.
old-location: direct3d11\id3d11linker.htm
tech.root: direct3d11
ms.assetid: 08967A5F-AAAE-4352-A8A9-C7B1ED16EF25
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11Linker, ID3D11Linker interface [Direct3D 11], ID3D11Linker interface [Direct3D 11],described, d3d11shader/ID3D11Linker, direct3d11.id3d11linker
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11Linker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Linker interface


## -description


A linker interface is used to link a shader module. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Linker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11Linker</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0E7820F1-8F4E-43B2-A8DD-560BC2B5BC3D">AddClipPlaneFromCBuffer</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://msdn.microsoft.com/C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11">clip plane</a> with the plane coefficients taken from a <a href="https://msdn.microsoft.com/89fe874a-8009-4901-bebe-2d9e45f894bb">cbuffer</a> entry for 10Level9 shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCEAE5C2-38E4-4B8F-BA98-F46B187FC586">Link</a>
</td>
<td align="left" width="63%">
Links the shader and produces a shader blob that the Direct3D runtime can use.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2FEA3583-8868-4763-8308-3C1E8F72A9BC">UseLibrary</a>
</td>
<td align="left" width="63%">
Adds an instance of a library module to be used for linking.

</td>
</tr>
</table> 


## -remarks



To get a linker interface, call <a href="https://msdn.microsoft.com/15BEFF31-9E08-462F-9F27-1CADB8367E4F">D3DCreateLinker</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11Linker</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

