---
UID: NF:d3d9helper.IDirect3DBaseTexture9.SetAutoGenFilterType
title: IDirect3DBaseTexture9::SetAutoGenFilterType
author: windows-driver-content
description: Set the filter type that is used for automatically generated mipmap sublevels.
old-location: direct3d9\idirect3dbasetexture9__setautogenfiltertype.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__setautogenfiltertype.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: 9d229d50-5ad7-e9ba-b0c4-0bf1f4d7f591, IDirect3DBaseTexture9 interface [Direct3D 9],SetAutoGenFilterType method, IDirect3DBaseTexture9.SetAutoGenFilterType, IDirect3DBaseTexture9::SetAutoGenFilterType, SetAutoGenFilterType, SetAutoGenFilterType method [Direct3D 9], SetAutoGenFilterType method [Direct3D 9],IDirect3DBaseTexture9 interface, d3d9helper/IDirect3DBaseTexture9::SetAutoGenFilterType, direct3d9.idirect3dbasetexture9__setautogenfiltertype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9helper.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DBaseTexture9.SetAutoGenFilterType
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DBaseTexture9::SetAutoGenFilterType


## -description


Set the filter type that is used for automatically generated mipmap sublevels.


## -parameters




### -param FilterType [in]

Type: <b><a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a></b>

Filter type. See <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>. This method will fail if the filter type is invalid or not supported.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Changing the filter type "dirties" the mipmap sublevels and causes them to be regenerated.

The (default) filter type set at texture creation time is D3DTEXF_LINEAR. If the driver does not support a linear filter, the filter type will be set to D3DTEXF_POINT. All filter types supported by the driver for regular texture filtering are supported for autogeneration except D3DTEXF_NONE. <b>SetAutoGenFilterType</b> will fail unless the driver sets the appropriate D3DPTFILTERCAPS_MINFxxx caps. These values are specified in the TextureFilterCaps and/or  CubeTextureFilterCaps members of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>. 
    
    For more information about texture filter types, see <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>.

This method has no effect if the texture is not created with D3DUSAGE_AUTOGENMIPMAP. In this case, no failure is returned. For more information about usage constants, see <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>.




## -see-also




<a href="https://msdn.microsoft.com/4fd7fcb3-d3fc-4db9-a56b-d5008e32c0c7">GenerateMipSubLevels</a>



<a href="https://msdn.microsoft.com/5dd29318-ddf3-4d21-9b6e-fa0e2512a004">GetAutoGenFilterType</a>



<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>
 

 

