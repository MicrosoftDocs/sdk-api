---
UID: NF:amvideo.IDirectDrawVideo.SetDirectDraw
title: IDirectDrawVideo::SetDirectDraw
author: windows-sdk-content
description: The SetDirectDraw method passes the IDirectDraw interface to a loaded driver.
old-location: dshow\idirectdrawvideo_setdirectdraw.htm
old-project: DirectShow
ms.assetid: fd7b9571-2edb-4f36-b7a3-b280c37cb471
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],SetDirectDraw method, IDirectDrawVideo.SetDirectDraw, IDirectDrawVideo::SetDirectDraw, IDirectDrawVideoSetDirectDraw, SetDirectDraw, SetDirectDraw method [DirectShow], SetDirectDraw method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::SetDirectDraw, dshow.idirectdrawvideo_setdirectdraw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawVideo.SetDirectDraw
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawVideo::SetDirectDraw


## -description



The <code>SetDirectDraw</code> method passes the <b>IDirectDraw</b> interface to a loaded driver.




## -parameters




### -param pDirectDraw

Pointer to the <b>IDirectDraw</b> interface to be passed.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



To have the renderer release a DirectDraw interface previously passed in through <code>SetDirectDraw</code>, an application can call <code>SetDirectDraw</code> and pass in <b>NULL</b>. However, the renderer will continue using that DirectDraw interface until it is disconnected. Therefore, calling <code>SetDirectDraw</code> with a <b>NULL</b> parameter does not make the renderer stop using it immediately.

This method was created because only one instance of <b>IDirectDraw</b> could be loaded per process in versions of DirectDraw prior to DirectX 7.0. If you are using DirectX 7.0 or later, you never need to call this method. If an application wanted to load <b>IDirectDraw</b> but allow the Video Renderer to also allocate surfaces, the application could open <b>IDirectDraw</b> itself and then pass the interface to the loaded driver through <code>IDirectDrawVideo::SetDirectDraw</code>. Alternatively, the application could let the renderer load DirectDraw and then obtain a reference-incremented interface to it through <a href="https://msdn.microsoft.com/25c64d6e-fd49-430a-9f9b-3c2b3d43d3a1">IDirectDrawVideo::GetDirectDraw</a>. Because DirectShow ships with the most recently shipped version of DirectDraw, however, this method is not required unless the application wants to change display modes itself and pass in a DirectDraw object, which the renderer can then use to allocate surfaces.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

