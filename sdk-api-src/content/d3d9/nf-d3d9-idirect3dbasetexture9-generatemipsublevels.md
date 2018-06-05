---
UID: NF:d3d9.IDirect3DBaseTexture9.GenerateMipSubLevels
title: IDirect3DBaseTexture9::GenerateMipSubLevels
author: windows-sdk-content
description: Generate mipmap sublevels.
old-location: direct3d9\idirect3dbasetexture9__generatemipsublevels.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__generatemipsublevels.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 7228ab65-d7b2-7a27-b076-d7bdec0f0e33, GenerateMipSubLevels, GenerateMipSubLevels method [Direct3D 9], GenerateMipSubLevels method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GenerateMipSubLevels method, IDirect3DBaseTexture9.GenerateMipSubLevels, IDirect3DBaseTexture9::GenerateMipSubLevels, d3d9helper/IDirect3DBaseTexture9::GenerateMipSubLevels, direct3d9.idirect3dbasetexture9__generatemipsublevels
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DBaseTexture9.GenerateMipSubLevels
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DBaseTexture9::GenerateMipSubLevels


## -description


Generate mipmap sublevels.


## -parameters






## -returns



No return value.




## -remarks



An application can generate mipmap sublevels at any time by calling <b>GenerateMipSubLevels</b>. To have mipmap sublevels generated automatically at texture creation time (see <a href="https://msdn.microsoft.com/ae5955f9-e52a-41d7-a199-800e37a3e936">Automatic Generation of Mipmaps (Direct3D 9)</a>), specify  D3DUSAGE_AUTOGENMIPMAP during <a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">CreateTexture</a>, <a href="https://msdn.microsoft.com/d8ae94bb-5b16-4d08-aeb9-cb15029725c9">CreateCubeTexture</a>, and <a href="https://msdn.microsoft.com/a0dada01-aca1-46ef-8321-62022219843f">CreateVolumeTexture</a>. For more information about usage constants, see <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>.




## -see-also




<a href="https://msdn.microsoft.com/5dd29318-ddf3-4d21-9b6e-fa0e2512a004">GetAutoGenFilterType</a>



<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/fa742bfe-e4b2-48f6-8d84-3772b519aab3">SetAutoGenFilterType</a>
 

 

