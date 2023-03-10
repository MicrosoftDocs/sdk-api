---
UID: NF:d3d9.IDirect3DBaseTexture9.GetAutoGenFilterType
title: IDirect3DBaseTexture9::GetAutoGenFilterType (d3d9.h)
description: The IDirect3DBaseTexture9::GetAutoGenFilterType method (d3d9helper.h) gets the filter type that is used for automatically generated mipmap sublevels.
helpviewer_keywords: ["7a155e44-4ee7-ac87-0ef7-42daed0b87ba","GetAutoGenFilterType","GetAutoGenFilterType method [Direct3D 9]","GetAutoGenFilterType method [Direct3D 9]","IDirect3DBaseTexture9 interface","IDirect3DBaseTexture9 interface [Direct3D 9]","GetAutoGenFilterType method","IDirect3DBaseTexture9.GetAutoGenFilterType","IDirect3DBaseTexture9::GetAutoGenFilterType","d3d9helper/IDirect3DBaseTexture9::GetAutoGenFilterType","direct3d9.idirect3dbasetexture9__getautogenfiltertype"]
old-location: direct3d9\idirect3dbasetexture9__getautogenfiltertype.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__getautogenfiltertype.htm
ms.date: 08/10/2022
ms.keywords: 7a155e44-4ee7-ac87-0ef7-42daed0b87ba, GetAutoGenFilterType, GetAutoGenFilterType method [Direct3D 9], GetAutoGenFilterType method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GetAutoGenFilterType method, IDirect3DBaseTexture9.GetAutoGenFilterType, IDirect3DBaseTexture9::GetAutoGenFilterType, d3d9helper/IDirect3DBaseTexture9::GetAutoGenFilterType, direct3d9.idirect3dbasetexture9__getautogenfiltertype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DBaseTexture9::GetAutoGenFilterType
 - d3d9/IDirect3DBaseTexture9::GetAutoGenFilterType
dev_langs:
 - c++
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
---

# IDirect3DBaseTexture9::GetAutoGenFilterType


## -description

Get the filter type that is used for automatically generated mipmap sublevels.



## -returns

Type: <b><a href="/windows/desktop/direct3d9/d3dtexturefiltertype">D3DTEXTUREFILTERTYPE</a></b>

Filter type. See <a href="/windows/desktop/direct3d9/d3dtexturefiltertype">D3DTEXTUREFILTERTYPE</a>. A texture must be created with <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE_AUTOGENMIPMAP</a> to use this method. Any other usage value will cause this method to return D3DTEXF_NONE.

## -remarks

Changing the filter type "dirties" the mipmap sublevels and causes them to be regenerated.

The (default) filter type set at texture creation time is D3DTEXF_LINEAR. If the driver doesn't support a linear filter, the filter type will be set to D3DTEXF_POINT. All filter types supported by the driver for regular texture filtering are supported for autogeneration except D3DTEXF_NONE. For each resource type, drivers should support all the filter types reported in the corresponding texture, CubeTexture, and volumetexture filter caps. For more information about texture types, see <a href="/windows/desktop/direct3d9/d3dtexturefiltertype">D3DTEXTUREFILTERTYPE</a>.

This method has no effect if the texture is not created with <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE_AUTOGENMIPMAP</a>.

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-generatemipsublevels">GenerateMipSubLevels</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-setautogenfiltertype">SetAutoGenFilterType</a>
