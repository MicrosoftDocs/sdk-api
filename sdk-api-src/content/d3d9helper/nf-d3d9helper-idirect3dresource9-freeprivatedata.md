---
UID: NF:d3d9helper.IDirect3DResource9.FreePrivateData
title: IDirect3DResource9::FreePrivateData
author: windows-sdk-content
description: Frees the specified private data associated with this resource.
old-location: direct3d9\idirect3dresource9__freeprivatedata.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__freeprivatedata.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FreePrivateData, FreePrivateData method [Direct3D 9], FreePrivateData method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],FreePrivateData method, IDirect3DResource9.FreePrivateData, IDirect3DResource9::FreePrivateData, d3d9helper/IDirect3DResource9::FreePrivateData, direct3d9.idirect3dresource9__freeprivatedata, e283eb7c-b7c9-110d-2b8b-1966dc1dc914
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DResource9.FreePrivateData
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DResource9::FreePrivateData


## -description


Frees the specified private data associated with this resource.


## -parameters




### -param refguid [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to free.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_NOTFOUND.




## -remarks



Direct3D calls this method automatically when a resource is released.




## -see-also




<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>
 

 

