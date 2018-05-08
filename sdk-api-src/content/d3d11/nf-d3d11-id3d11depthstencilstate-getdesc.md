---
UID: NF:d3d11.ID3D11DepthStencilState.GetDesc
title: ID3D11DepthStencilState::GetDesc
author: windows-driver-content
description: Gets the description for depth-stencil state that you used to create the depth-stencil-state object.
old-location: direct3d11\id3d11depthstencilstate_getdesc.htm
old-project: direct3d11
ms.assetid: f83ee1cf-b435-4c10-afb6-916307c420f9
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11DepthStencilState interface, ID3D11DepthStencilState interface [Direct3D 11],GetDesc method, ID3D11DepthStencilState.GetDesc, ID3D11DepthStencilState::GetDesc, b5b2c6e1-1315-e15e-9d66-a15b16d828aa, d3d11/ID3D11DepthStencilState::GetDesc, direct3d11.id3d11depthstencilstate_getdesc
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DepthStencilState.GetDesc
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DepthStencilState::GetDesc


## -description


Gets the description for depth-stencil state that you used to create the depth-stencil-state object.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a> structure that receives a description of the depth-stencil state.


## -returns



Returns nothing.




## -remarks



You use the description for depth-stencil state in a call to the <a href="https://msdn.microsoft.com/7577604c-922c-408c-8eab-2361ebda17df">ID3D11Device::CreateDepthStencilState</a> method to create the depth-stencil-state object.




## -see-also




<a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>
 

 

