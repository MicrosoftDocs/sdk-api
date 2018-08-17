---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearState
title: ID3D12GraphicsCommandList::ClearState
author: windows-sdk-content
description: Resets the state of a direct command list back to the state it was in when the command list was created.
old-location: direct3d12\id3d12graphicscommandlist_clearstate.htm
old-project: direct3d12
ms.assetid: F7C230CE-0E28-466A-8A54-601ECEC6CDC9
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ClearState, ClearState method, ClearState method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearState method, ID3D12GraphicsCommandList.ClearState, ID3D12GraphicsCommandList::ClearState, d3d12/ID3D12GraphicsCommandList::ClearState, direct3d12.id3d12graphicscommandlist_clearstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList.ClearState
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::ClearState


## -description


Resets the state of a direct command list back to the state it was in when the command list was created.  


## -parameters




### -param pPipelineState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn788705(v=VS.85).aspx">ID3D12PipelineState</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn788705(v=VS.85).aspx">ID3D12PipelineState</a> object that contains the initial pipeline state for the command list.
          


## -returns



Returns nothing.
          




## -remarks



It is invalid to call <b>ClearState</b> on a bundle.  If an app calls <b>ClearState</b> on a bundle, the call to <a href="https://msdn.microsoft.com/en-us/library/Dn903855(v=VS.85).aspx">Close</a> will return <b>E_FAIL</b>.
      

When <b>ClearState</b> is called, all currently bound resources are unbound.  The primitive topology is set to <a href="https://msdn.microsoft.com/en-us/library/Ff728726(v=VS.85).aspx">D3D_PRIMITIVE_TOPOLOGY_UNDEFINED</a>.  Viewports, scissor rectangles, stencil reference value, and the blend factor are set to empty values (all zeros).  Predication is disabled.
      

The app-provided pipeline state object becomes bound as the currently set pipeline state object.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn903537(v=VS.85).aspx">ID3D12GraphicsCommandList</a>
 

 

