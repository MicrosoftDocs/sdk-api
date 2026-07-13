---
UID: NN:d3d11shader.ID3D11ModuleInstance
title: ID3D11ModuleInstance (d3d11shader.h)
description: A module-instance interface is used for resource rebinding.
helpviewer_keywords: ["ID3D11ModuleInstance","ID3D11ModuleInstance interface [Direct3D 11]","ID3D11ModuleInstance interface [Direct3D 11]","described","d3d11shader/ID3D11ModuleInstance","direct3d11.id3d11moduleinstance"]
old-location: direct3d11\id3d11moduleinstance.htm
tech.root: direct3d11
ms.assetid: BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5
ms.date: 12/05/2018
ms.keywords: ID3D11ModuleInstance, ID3D11ModuleInstance interface [Direct3D 11], ID3D11ModuleInstance interface [Direct3D 11],described, d3d11shader/ID3D11ModuleInstance, direct3d11.id3d11moduleinstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ModuleInstance
 - d3d11shader/ID3D11ModuleInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ModuleInstance
---

# ID3D11ModuleInstance interface


## -description

A module-instance interface is used for resource rebinding. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>

## -inheritance

The <b>ID3D11ModuleInstance</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ModuleInstance</b> also has these types of members:

## -remarks

To get a module-instance interface, call <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance">ID3D11Module::CreateInstance</a> or <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance">ID3D11FunctionLinkingGraph::CreateModuleInstance</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11ModuleInstance</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
