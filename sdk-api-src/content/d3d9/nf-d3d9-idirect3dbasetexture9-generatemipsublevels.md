---
UID: NF:d3d9.IDirect3DBaseTexture9.GenerateMipSubLevels
title: IDirect3DBaseTexture9::GenerateMipSubLevels
author: windows-sdk-content
description: Generate mipmap sublevels.
old-location: direct3d9\idirect3dbasetexture9__generatemipsublevels.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__generatemipsublevels.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 7228ab65-d7b2-7a27-b076-d7bdec0f0e33, GenerateMipSubLevels, GenerateMipSubLevels method [Direct3D 9], GenerateMipSubLevels method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GenerateMipSubLevels method, IDirect3DBaseTexture9.GenerateMipSubLevels, IDirect3DBaseTexture9::GenerateMipSubLevels, d3d9helper/IDirect3DBaseTexture9::GenerateMipSubLevels, direct3d9.idirect3dbasetexture9__generatemipsublevels
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
 - IDirect3DBaseTexture9.GenerateMipSubLevels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9.h
: 
- IDirect3DBaseTexture9.GenerateMipSubLevels
: 
---

# IDirect3DBaseTexture9::GenerateMipSubLevels


## -description


Generate mipmap sublevels.


## -parameters






## -returns



No return value.




## -remarks



An application can generate mipmap sublevels at any time by calling <b>GenerateMipSubLevels</b>. To have mipmap sublevels generated automatically at texture creation time (see <a href="https://msdn.microsoft.com/en-us/library/Bb172340(v=VS.85).aspx">Automatic Generation of Mipmaps (Direct3D 9)</a>), specify  D3DUSAGE_AUTOGENMIPMAP during <a href="https://msdn.microsoft.com/en-us/library/Bb174363(v=VS.85).aspx">CreateTexture</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb174355(v=VS.85).aspx">CreateCubeTexture</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb174367(v=VS.85).aspx">CreateVolumeTexture</a>. For more information about usage constants, see <a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">D3DUSAGE</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174324(v=VS.85).aspx">GetAutoGenFilterType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174327(v=VS.85).aspx">SetAutoGenFilterType</a>
 

 

