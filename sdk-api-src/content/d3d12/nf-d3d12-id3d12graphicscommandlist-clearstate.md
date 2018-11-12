---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearState
title: ID3D12GraphicsCommandList::ClearState
author: windows-sdk-content
description: Resets the state of a direct command list back to the state it was in when the command list was created.
old-location: direct3d12\id3d12graphicscommandlist_clearstate.htm
tech.root: direct3d12
ms.assetid: F7C230CE-0E28-466A-8A54-601ECEC6CDC9
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ClearState, ClearState method, ClearState method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearState method, ID3D12GraphicsCommandList.ClearState, ID3D12GraphicsCommandList::ClearState, d3d12/ID3D12GraphicsCommandList::ClearState, direct3d12.id3d12graphicscommandlist_clearstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::ClearState


## -description


Resets the state of a direct command list back to the state it was in when the command list was created.  


## -parameters




### -param pPipelineState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> object that contains the initial pipeline state for the command list.
          


## -returns



Returns nothing.
          




## -remarks



It is invalid to call <b>ClearState</b> on a bundle.  If an app calls <b>ClearState</b> on a bundle, the call to <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> will return <b>E_FAIL</b>.
      

When <b>ClearState</b> is called, all currently bound resources are unbound.  The primitive topology is set to <a href="https://msdn.microsoft.com/b4becdcc-cc19-4d5a-940b-b232ebedce68">D3D_PRIMITIVE_TOPOLOGY_UNDEFINED</a>.  Viewports, scissor rectangles, stencil reference value, and the blend factor are set to empty values (all zeros).  Predication is disabled.
      

The app-provided pipeline state object becomes bound as the currently set pipeline state object.
      




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

