---
UID: NN:d3d11shader.ID3D11Module
title: ID3D11Module
author: windows-sdk-content
description: A module interface creates an instance of a module that is used for resource rebinding.
old-location: direct3d11\id3d11module.htm
old-project: direct3d11
ms.assetid: 5915DACB-1D3A-496C-96C6-77D85CC6560B
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: ID3D11Module, ID3D11Module interface [Direct3D 11], ID3D11Module interface [Direct3D 11],described, d3d11shader/ID3D11Module, direct3d11.id3d11module
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11Module
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11Module interface


## -description



          A module interface creates an instance of a module that is used for resource rebinding. <div class="alert"><b>Note</b>  
            This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Module</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11Module</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Module</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/737A69EF-F74E-4480-98EA-31D6CCAC0F8A">CreateInstance</a>
</td>
<td align="left" width="63%">
Initializes an instance of a shader module that is used for resource rebinding.

</td>
</tr>
</table> 


## -remarks




        To get a module interface, call <a href="https://msdn.microsoft.com/698AADA6-0A88-44AD-9F15-F085BFE52CA1">D3DLoadModule</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11Module</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

