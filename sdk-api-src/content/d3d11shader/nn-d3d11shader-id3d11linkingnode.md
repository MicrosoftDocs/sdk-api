---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11LinkingNode interface


## -description



          A linking-node interface is used for shader linking. <div class="alert"><b>Note</b>  
            This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
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
 

 

