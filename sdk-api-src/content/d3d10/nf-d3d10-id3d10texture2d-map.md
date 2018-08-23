---
UID: NF:d3d10.ID3D10Texture2D.Map
title: ID3D10Texture2D::Map
author: windows-sdk-content
description: Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.
old-location: direct3d10\id3d10texture2d_map.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture2d_map.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 2f53ee75-643c-3909-1e4f-aa32b40994c3, ID3D10Texture2D interface [Direct3D 10],Map method, ID3D10Texture2D.Map, ID3D10Texture2D::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Texture2D interface, d3d10/ID3D10Texture2D::Map, direct3d10.id3d10texture2d_map
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Texture2D.Map
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture2D::Map


## -description


Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index number of the subresource. See <a href="https://msdn.microsoft.com/48079797-b5c8-487b-a343-a5623b780350">D3D10CalcSubresource</a> for more details.


### -param MapType [in]

Type: <b><a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP</a></b>

Integer that specifies the CPU's read and write permissions for a resource. For possible values, see <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP</a>.


### -param MapFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/cc8a1dae-4a48-4894-8ef4-67289062400d">Flag</a> that specifies what the CPU should do when the GPU is busy. This flag is optional.


### -param pMappedTex2D [out]

Type: <b><a href="https://msdn.microsoft.com/7c56991a-9364-4e2d-b681-38d007d31fad">D3D10_MAPPED_TEXTURE2D</a>*</b>

Pointer to a structure (<a href="https://msdn.microsoft.com/7c56991a-9364-4e2d-b681-38d007d31fad">D3D10_MAPPED_TEXTURE2D</a>) that is filled in by the function and contains a pointer to the resource data.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns S_OK.

All of the Map methods have identical return values and operating restrictions. These are listed in the remarks section of <a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">ID3D10Texture1D::Map</a>.




## -see-also




<a href="https://msdn.microsoft.com/87e9a9ee-7e73-4f3c-8898-c8bbfe6508c2">ID3D10Texture2D Interface</a>
 

 

