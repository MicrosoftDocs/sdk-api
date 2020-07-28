---
UID: NN:d3d11shader.ID3D11LinkingNode
title: ID3D11LinkingNode (d3d11shader.h)
description: A linking-node interface is used for shader linking.
helpviewer_keywords: ["ID3D11LinkingNode","ID3D11LinkingNode interface [Direct3D 11]","ID3D11LinkingNode interface [Direct3D 11]","described","d3d11shader/ID3D11LinkingNode","direct3d11.id3d11linkingnode"]
old-location: direct3d11\id3d11linkingnode.htm
tech.root: direct3d11
ms.assetid: 533D2DA8-107A-48B1-928F-5788DC9CF706
ms.date: 12/05/2018
ms.keywords: ID3D11LinkingNode, ID3D11LinkingNode interface [Direct3D 11], ID3D11LinkingNode interface [Direct3D 11],described, d3d11shader/ID3D11LinkingNode, direct3d11.id3d11linkingnode
f1_keywords:
- d3d11shader/ID3D11LinkingNode
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
- ID3D11LinkingNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11LinkingNode interface


## -description


A linking-node interface is used for shader linking. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -remarks



To get a linking-node interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature">ID3D11FunctionLinkingGraph::SetInputSignature</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature">ID3D11FunctionLinkingGraph::SetOutputSignature</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction">ID3D11FunctionLinkingGraph::CallFunction</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11LinkingNode</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

