---
UID: NF:amvideo.IDirectDrawVideo.SetDirectDraw
title: IDirectDrawVideo::SetDirectDraw (amvideo.h)
author: windows-sdk-content
description: The SetDirectDraw method passes the IDirectDraw interface to a loaded driver.
old-location: dshow\idirectdrawvideo_setdirectdraw.htm
tech.root: DirectShow
ms.assetid: fd7b9571-2edb-4f36-b7a3-b280c37cb471
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],SetDirectDraw method, IDirectDrawVideo.SetDirectDraw, IDirectDrawVideo::SetDirectDraw, IDirectDrawVideoSetDirectDraw, SetDirectDraw, SetDirectDraw method [DirectShow], SetDirectDraw method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::SetDirectDraw, dshow.idirectdrawvideo_setdirectdraw
ms.topic: method
f1_keywords: 
 - "amvideo/IDirectDrawVideo.SetDirectDraw"
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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

This method was created because only one instance of <b>IDirectDraw</b> could be loaded per process in versions of DirectDraw prior to DirectX 7.0. If you are using DirectX 7.0 or later, you never need to call this method. If an application wanted to load <b>IDirectDraw</b> but allow the Video Renderer to also allocate surfaces, the application could open <b>IDirectDraw</b> itself and then pass the interface to the loaded driver through <code>IDirectDrawVideo::SetDirectDraw</code>. Alternatively, the application could let the renderer load DirectDraw and then obtain a reference-incremented interface to it through <a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getdirectdraw">IDirectDrawVideo::GetDirectDraw</a>. Because DirectShow ships with the most recently shipped version of DirectDraw, however, this method is not required unless the application wants to change display modes itself and pass in a DirectDraw object, which the renderer can then use to allocate surfaces.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>
 

 

