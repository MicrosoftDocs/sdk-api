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
 

 

