---
UID: NF:d3d11.ID3D11DeviceContext.RSGetState
title: ID3D11DeviceContext::RSGetState
author: windows-sdk-content
description: Get the rasterizer state from the rasterizer stage of the pipeline.
old-location: direct3d11\id3d11devicecontext_rsgetstate.htm
old-project: direct3d11
ms.assetid: bd1ade36-e57c-4776-ab59-ba8b59276369
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: 7de5d766-760e-6053-6c62-f66f824404ea, ID3D11DeviceContext interface [Direct3D 11],RSGetState method, ID3D11DeviceContext.RSGetState, ID3D11DeviceContext::RSGetState, RSGetState, RSGetState method [Direct3D 11], RSGetState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSGetState, direct3d11.id3d11devicecontext_rsgetstate
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
 - ID3D11DeviceContext.RSGetState
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::RSGetState


## -description


Get the <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">rasterizer state</a> from the rasterizer stage of the pipeline.


## -parameters




### -param ppRasterizerState [out]

Type: <b><a href="https://msdn.microsoft.com/fbe6d2b9-375e-4390-9d34-36acef0a5aa2">ID3D11RasterizerState</a>**</b>

Address of a pointer to a rasterizer-state interface (see <a href="https://msdn.microsoft.com/fbe6d2b9-375e-4390-9d34-36acef0a5aa2">ID3D11RasterizerState</a>) to fill with information from the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

