---
UID: NN:d3d11shader.ID3D11LinkingNode
title: ID3D11LinkingNode
author: windows-sdk-content
description: A linking-node interface is used for shader linking.
old-location: direct3d11\id3d11linkingnode.htm
tech.root: direct3d11
ms.assetid: 533D2DA8-107A-48B1-928F-5788DC9CF706
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11LinkingNode, ID3D11LinkingNode interface [Direct3D 11], ID3D11LinkingNode interface [Direct3D 11],described, d3d11shader/ID3D11LinkingNode, direct3d11.id3d11linkingnode
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
 - ID3D11LinkingNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11LinkingNode interface


## -description


A linking-node interface is used for shader linking. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -remarks



To get a linking-node interface, call <a href="https://msdn.microsoft.com/9108BA38-6A0A-4438-BC63-A80790E4A5F0">ID3D11FunctionLinkingGraph::SetInputSignature</a>, <a href="https://msdn.microsoft.com/C32E3BF1-E08C-4949-A8DE-4359704D2E40">ID3D11FunctionLinkingGraph::SetOutputSignature</a>, or <a href="https://msdn.microsoft.com/0DEEE3E4-7D4E-40BD-9D96-A1C91CF5E4BE">ID3D11FunctionLinkingGraph::CallFunction</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11LinkingNode</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

