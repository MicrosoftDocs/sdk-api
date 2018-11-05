---
UID: NF:d3d9.IDirect3DBaseTexture9.GetAutoGenFilterType
title: IDirect3DBaseTexture9::GetAutoGenFilterType
author: windows-sdk-content
description: Get the filter type that is used for automatically generated mipmap sublevels.
old-location: direct3d9\idirect3dbasetexture9__getautogenfiltertype.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__getautogenfiltertype.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 7a155e44-4ee7-ac87-0ef7-42daed0b87ba, GetAutoGenFilterType, GetAutoGenFilterType method [Direct3D 9], GetAutoGenFilterType method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GetAutoGenFilterType method, IDirect3DBaseTexture9.GetAutoGenFilterType, IDirect3DBaseTexture9::GetAutoGenFilterType, d3d9helper/IDirect3DBaseTexture9::GetAutoGenFilterType, direct3d9.idirect3dbasetexture9__getautogenfiltertype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DBaseTexture9.GetAutoGenFilterType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

