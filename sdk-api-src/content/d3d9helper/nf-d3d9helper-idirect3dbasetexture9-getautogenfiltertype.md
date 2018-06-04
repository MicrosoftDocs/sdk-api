---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DBaseTexture9::GetAutoGenFilterType


## -description


Get the filter type that is used for automatically generated mipmap sublevels.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a></b>

Filter type. See <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>. A texture must be created with <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_AUTOGENMIPMAP</a> to use this method. Any other usage value will cause this method to return D3DTEXF_NONE.




## -remarks



Changing the filter type "dirties" the mipmap sublevels and causes them to be regenerated.

The (default) filter type set at texture creation time is D3DTEXF_LINEAR. If the driver doesn't support a linear filter, the filter type will be set to D3DTEXF_POINT. All filter types supported by the driver for regular texture filtering are supported for autogeneration except D3DTEXF_NONE. For each resource type, drivers should support all the filter types reported in the corresponding texture, CubeTexture, and volumetexture filter caps. For more information about texture types, see <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>.

This method has no effect if the texture is not created with <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_AUTOGENMIPMAP</a>.




## -see-also




<a href="https://msdn.microsoft.com/4fd7fcb3-d3fc-4db9-a56b-d5008e32c0c7">GenerateMipSubLevels</a>



<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/fa742bfe-e4b2-48f6-8d84-3772b519aab3">SetAutoGenFilterType</a>
 

 

