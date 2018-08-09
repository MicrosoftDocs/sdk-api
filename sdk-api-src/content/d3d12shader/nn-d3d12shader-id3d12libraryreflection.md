---
UID: NN:d3d12shader.ID3D12LibraryReflection
title: ID3D12LibraryReflection
author: windows-sdk-content
description: A library-reflection interface accesses library info.
old-location: direct3d12\id3d12libraryreflection.htm
old-project: direct3d12
ms.assetid: CE6AEA77-A6A0-46A5-BDBC-AE4907AAC820
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12LibraryReflection, ID3D12LibraryReflection interface, ID3D12LibraryReflection interface,described, d3d12shader/ID3D12LibraryReflection, direct3d12.id3d12libraryreflection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12LibraryReflection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12LibraryReflection interface


## -description


A library-reflection interface accesses library info.
          <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12LibraryReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12LibraryReflection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/BF7CC078-3F68-4645-B49C-1F4DEBCA6A48">GetDesc</a>
</td>
<td align="left" width="63%">
Fills the library descriptor structure for the library reflection.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1600824A-6C9E-4C87-8D6B-07F299D47A53">GetFunctionByIndex</a>
</td>
<td align="left" width="63%">
Gets the function reflector.
        

</td>
</tr>
</table> 


## -remarks



To get a library-reflection interface, call <a href="https://msdn.microsoft.com/E64FB2C3-8F64-411F-89E1-984DAAE4D7C2">D3DReflectLibrary</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D12LibraryReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/791d2c91-3791-47fe-b887-8117ecc798ba">Shader Interfaces</a>
 

 

