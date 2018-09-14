---
UID: NS:d3d11_3.D3D11_UNORDERED_ACCESS_VIEW_DESC1
title: D3D11_UNORDERED_ACCESS_VIEW_DESC1
author: windows-sdk-content
description: Describes the subresources from a resource that are accessible using an unordered-access view.
old-location: direct3d11\d3d11_unordered_access_view_desc1.htm
tech.root: direct3d11
ms.assetid: 833B4B8A-5702-4C17-AFD2-DFDF69354DDD
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CD3D11_UNORDERED_ACCESS_VIEW_DESC1, D3D11_UNORDERED_ACCESS_VIEW_DESC1, D3D11_UNORDERED_ACCESS_VIEW_DESC1 structure [Direct3D 11], d3d11_3/D3D11_UNORDERED_ACCESS_VIEW_DESC1, direct3d11.d3d11_unordered_access_view_desc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_3.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_UNORDERED_ACCESS_VIEW_DESC1
product: Windows
targetos: Windows
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
req.redist: 
---

# D3D11_UNORDERED_ACCESS_VIEW_DESC1 structure


## -description


Describes the subresources from a resource that are accessible using an unordered-access view.


## -struct-fields




#### - Format

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that specifies the data format.


#### - ViewDimension

A <a href="https://msdn.microsoft.com/en-us/library/Ff476257(v=VS.85).aspx">D3D11_UAV_DIMENSION</a>-typed value that  specifies the resource type of the view. This type is the same as the resource type of the underlying resource. This member also determines which _UAV to use in the union below.


#### - Buffer

A <a href="https://msdn.microsoft.com/en-us/library/Ff476095(v=VS.85).aspx">D3D11_BUFFER_UAV</a> structure that specifies which buffer elements can be accessed.


#### - Texture1D

A <a href="https://msdn.microsoft.com/en-us/library/Ff476232(v=VS.85).aspx">D3D11_TEX1D_UAV</a> structure that specifies the subresources in a 1D texture that can be accessed.


#### - Texture1DArray

A <a href="https://msdn.microsoft.com/en-us/library/Ff476228(v=VS.85).aspx">D3D11_TEX1D_ARRAY_UAV</a> structure that specifies the subresources in a 1D texture array that can be accessed.


#### - Texture2D

A <a href="https://msdn.microsoft.com/en-us/library/Dn899165(v=VS.85).aspx">D3D11_TEX2D_UAV1</a> structure that specifies the subresources in a 2D texture that can be accessed.


#### - Texture2DArray

A <a href="https://msdn.microsoft.com/en-us/library/Dn899162(v=VS.85).aspx">D3D11_TEX2D_ARRAY_UAV1</a> structure that specifies the subresources in a 2D texture array that can be accessed.


#### - Texture3D

A <a href="https://msdn.microsoft.com/en-us/library/Ff476249(v=VS.85).aspx">D3D11_TEX3D_UAV</a> structure that specifies subresources in a 3D texture that can be accessed.


## -remarks



An unordered-access-view description is passed into <a href="https://msdn.microsoft.com/AB64DDED-4C2D-4952-BAA5-3139F973C962">ID3D11Device3::CreateUnorderedAccessView1</a> to create a view.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

