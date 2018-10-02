---
UID: NF:d3d11.ID3D11DeviceContext.ClearState
title: ID3D11DeviceContext::ClearState
author: windows-sdk-content
description: Restore all default settings.
old-location: direct3d11\id3d11devicecontext_clearstate.htm
tech.root: direct3d11
ms.assetid: dabf52f5-0f69-4017-863c-9e3ecef4d5dc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClearState, ClearState method [Direct3D 11], ClearState method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearState method, ID3D11DeviceContext.ClearState, ID3D11DeviceContext::ClearState, b3d84ab3-64bc-1c6c-0a7d-5e4409b47dec, d3d11/ID3D11DeviceContext::ClearState, direct3d11.id3d11devicecontext_clearstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.ClearState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::ClearState


## -description


Restore all default settings.


## -parameters






## -returns



Returns nothing.




## -remarks



This method resets any device context to the default settings. This sets all input/output resource slots, shaders, input layouts, predications, scissor rectangles, depth-stencil state, rasterizer state, blend state, sampler state, and viewports to <b>NULL</b>. The primitive topology is set to UNDEFINED.

For a scenario where you would like to clear a list of commands recorded so far, call <a href="https://msdn.microsoft.com/31e9d8b6-4173-4999-8772-75134d60d269">ID3D11DeviceContext::FinishCommandList</a> and throw away the resulting <a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a>.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

