---
UID: NF:d3d9.IDirect3DBaseTexture9.GenerateMipSubLevels
title: IDirect3DBaseTexture9::GenerateMipSubLevels (d3d9.h)
description: The IDirect3DBaseTexture9::GenerateMipSubLevels method (d3d9helper.h) generates mipmap sublevels. 
helpviewer_keywords: ["7228ab65-d7b2-7a27-b076-d7bdec0f0e33","GenerateMipSubLevels","GenerateMipSubLevels method [Direct3D 9]","GenerateMipSubLevels method [Direct3D 9]","IDirect3DBaseTexture9 interface","IDirect3DBaseTexture9 interface [Direct3D 9]","GenerateMipSubLevels method","IDirect3DBaseTexture9.GenerateMipSubLevels","IDirect3DBaseTexture9::GenerateMipSubLevels","d3d9helper/IDirect3DBaseTexture9::GenerateMipSubLevels","direct3d9.idirect3dbasetexture9__generatemipsublevels"]
old-location: direct3d9\idirect3dbasetexture9__generatemipsublevels.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__generatemipsublevels.htm
ms.date: 08/10/2022
ms.keywords: 7228ab65-d7b2-7a27-b076-d7bdec0f0e33, GenerateMipSubLevels, GenerateMipSubLevels method [Direct3D 9], GenerateMipSubLevels method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GenerateMipSubLevels method, IDirect3DBaseTexture9.GenerateMipSubLevels, IDirect3DBaseTexture9::GenerateMipSubLevels, d3d9helper/IDirect3DBaseTexture9::GenerateMipSubLevels, direct3d9.idirect3dbasetexture9__generatemipsublevels
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
 - IDirect3DBaseTexture9::GenerateMipSubLevels
 - d3d9/IDirect3DBaseTexture9::GenerateMipSubLevels
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
 - IDirect3DBaseTexture9.GenerateMipSubLevels
---

# IDirect3DBaseTexture9::GenerateMipSubLevels


## -description

Generate mipmap sublevels.



## -remarks

An application can generate mipmap sublevels at any time by calling <b>GenerateMipSubLevels</b>. To have mipmap sublevels generated automatically at texture creation time (see <a href="/windows/desktop/direct3d9/automatic-generation-of-mipmaps">Automatic Generation of Mipmaps (Direct3D 9)</a>), specify  D3DUSAGE_AUTOGENMIPMAP during <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">CreateTexture</a>, <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">CreateCubeTexture</a>, and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">CreateVolumeTexture</a>. For more information about usage constants, see <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a>.

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getautogenfiltertype">GetAutoGenFilterType</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-setautogenfiltertype">SetAutoGenFilterType</a>
