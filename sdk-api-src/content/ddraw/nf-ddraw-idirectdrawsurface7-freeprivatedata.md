---
UID: NF:ddraw.IDirectDrawSurface7.FreePrivateData
title: IDirectDrawSurface7::FreePrivateData
author: windows-sdk-content
description: Frees the specified private data that is associated with this surface.
old-location: directdraw\idirectdrawsurface7_freeprivatedata.htm
old-project: directdraw
ms.assetid: 66d3f701-735c-4dca-b7b6-47a17d63c23e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FreePrivateData, FreePrivateData method [DirectDraw], FreePrivateData method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],FreePrivateData method, IDirectDrawSurface7.FreePrivateData, IDirectDrawSurface7::FreePrivateData, ddraw/IDirectDrawSurface7::FreePrivateData, directdraw.idirectdrawsurface7_freeprivatedata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.FreePrivateData
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::FreePrivateData


## -description


Frees the specified private data that is associated with this surface.


## -parameters






#### - guidTag [in]

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to be freed.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
</ul>



## -remarks



DirectDraw calls this method automatically when a surface is released.

If the private data was set by using the DDSPD_IUNKNOWNPOINTER flag, <b>FreePrivateData</b> calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the associated interface.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>FreePrivateData</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

