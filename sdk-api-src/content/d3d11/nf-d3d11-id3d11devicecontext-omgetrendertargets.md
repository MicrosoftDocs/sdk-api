---
UID: NF:d3d11.ID3D11DeviceContext.OMGetRenderTargets
title: ID3D11DeviceContext::OMGetRenderTargets
author: windows-sdk-content
description: Get pointers to the resources bound to the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omgetrendertargets.htm
old-project: direct3d11
ms.assetid: 27ac656a-0906-43ad-8089-b41639b55ecf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMGetRenderTargets method, ID3D11DeviceContext.OMGetRenderTargets, ID3D11DeviceContext::OMGetRenderTargets, OMGetRenderTargets, OMGetRenderTargets method [Direct3D 11], OMGetRenderTargets method [Direct3D 11],ID3D11DeviceContext interface, b914865b-766f-62c4-e7e9-5b7590860668, d3d11/ID3D11DeviceContext::OMGetRenderTargets, direct3d11.id3d11devicecontext_omgetrendertargets
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.OMGetRenderTargets
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::OMGetRenderTargets


## -description


Get pointers to the resources bound to the output-merger stage.


## -parameters




### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of render targets to retrieve.


### -param ppRenderTargetViews [out, optional]

Type: <b><a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>**</b>

Pointer to an array of <a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>s which represent render target views. Specify <b>NULL</b> for this parameter when retrieval of a render target is not needed. 


### -param ppDepthStencilView [out, optional]

Type: <b><a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a>**</b>

Pointer to a <a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a>, which represents a depth-stencil view. Specify <b>NULL</b> for this parameter when retrieval of the depth-stencil view is not needed.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

