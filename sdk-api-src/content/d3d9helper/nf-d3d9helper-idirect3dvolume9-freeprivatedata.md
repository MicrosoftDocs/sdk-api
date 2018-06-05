---
UID: NF:d3d9helper.IDirect3DVolume9.FreePrivateData
title: IDirect3DVolume9::FreePrivateData
author: windows-sdk-content
description: Frees the specified private data associated with this volume.
old-location: direct3d9\idirect3dvolume9__freeprivatedata.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__freeprivatedata.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: FreePrivateData, FreePrivateData method [Direct3D 9], FreePrivateData method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],FreePrivateData method, IDirect3DVolume9.FreePrivateData, IDirect3DVolume9::FreePrivateData, b68ae9e8-a0dd-1a8d-6653-dbbf3a1477d4, d3d9helper/IDirect3DVolume9::FreePrivateData, direct3d9.idirect3dvolume9__freeprivatedata
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IDirect3DVolume9.FreePrivateData
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVolume9::FreePrivateData


## -description


Frees the specified private data associated with this volume.


## -parameters




### -param refguid [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to free.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_NOTFOUND.




## -remarks



Direct3D calls this method automatically when a volume is released. 




## -see-also




<a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a>



<a href="https://msdn.microsoft.com/73f37211-b6e6-4007-8767-6f68fa026cb5">IDirect3DVolume9::GetPrivateData</a>



<a href="https://msdn.microsoft.com/e6d49e44-2633-4a11-8361-f8ea3b2b7d37">IDirect3DVolume9::SetPrivateData</a>
 

 

