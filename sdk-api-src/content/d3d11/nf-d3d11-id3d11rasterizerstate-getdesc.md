---
UID: NF:d3d11.ID3D11RasterizerState.GetDesc
title: ID3D11RasterizerState::GetDesc
author: windows-sdk-content
description: Gets the description for rasterizer state that you used to create the rasterizer-state object.
old-location: direct3d11\id3d11rasterizerstate_getdesc.htm
old-project: direct3d11
ms.assetid: cc6bbdd2-af9c-45be-a13a-5f9105f08c99
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11RasterizerState interface, ID3D11RasterizerState interface [Direct3D 11],GetDesc method, ID3D11RasterizerState.GetDesc, ID3D11RasterizerState::GetDesc, ce48f8a7-2b79-44f8-93db-80cad9b1ca3b, d3d11/ID3D11RasterizerState::GetDesc, direct3d11.id3d11rasterizerstate_getdesc
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
 - ID3D11RasterizerState.GetDesc
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11RasterizerState::GetDesc


## -description


Gets the description for rasterizer state that you used to create the rasterizer-state object.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">D3D11_RASTERIZER_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">D3D11_RASTERIZER_DESC</a> structure that receives a description of the rasterizer state.


## -returns



Returns nothing.




## -remarks



You use the description for rasterizer state in a call to the <a href="https://msdn.microsoft.com/b49a8dbb-2280-4d5d-ae65-58cde2e9ed10">ID3D11Device::CreateRasterizerState</a> method to create the rasterizer-state object.




## -see-also




<a href="https://msdn.microsoft.com/fbe6d2b9-375e-4390-9d34-36acef0a5aa2">ID3D11RasterizerState</a>
 

 

