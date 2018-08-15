---
UID: NF:d3d11_3.ID3D11RasterizerState2.GetDesc2
title: ID3D11RasterizerState2::GetDesc2
author: windows-sdk-content
description: Gets the description for rasterizer state that you used to create the rasterizer-state object.
old-location: direct3d11\id3d11rasterizerstate2_getdesc2.htm
old-project: direct3d11
ms.assetid: 23A3BCDF-9D3D-4984-BFA9-E598773DBC44
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDesc2, GetDesc2 method [Direct3D 11], GetDesc2 method [Direct3D 11],ID3D11RasterizerState2 interface, ID3D11RasterizerState2 interface [Direct3D 11],GetDesc2 method, ID3D11RasterizerState2.GetDesc2, ID3D11RasterizerState2::GetDesc2, d3d11_3/ID3D11RasterizerState2::GetDesc2, direct3d11.id3d11rasterizerstate2_getdesc2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11RasterizerState2.GetDesc2
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11RasterizerState2::GetDesc2


## -description


Gets the description for rasterizer state that you used to create the rasterizer-state object.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/54B5744A-1F50-4203-A43B-7E830D769534">D3D11_RASTERIZER_DESC2</a> structure that receives a description of the rasterizer state. This rasterizer state can specify forced sample count and conservative rasterization mode.
          


## -returns



Returns nothing.




## -remarks



You use the description for rasterizer state in a call to the <a href="https://msdn.microsoft.com/42BA8F50-7D86-4411-AE05-74F492761DBD">ID3D11Device3::CreateRasterizerState2</a> method to create the rasterizer-state object.




## -see-also




<a href="https://msdn.microsoft.com/335D976C-9E7F-4EAE-B671-F99D1B31669B">ID3D11RasterizerState2</a>
 

 

