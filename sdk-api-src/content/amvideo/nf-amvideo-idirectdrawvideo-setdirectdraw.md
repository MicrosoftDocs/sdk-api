---
UID: NF:amvideo.IDirectDrawVideo.SetDirectDraw
title: IDirectDrawVideo::SetDirectDraw (amvideo.h)
description: The SetDirectDraw method passes the IDirectDraw interface to a loaded driver.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","SetDirectDraw method","IDirectDrawVideo.SetDirectDraw","IDirectDrawVideo::SetDirectDraw","IDirectDrawVideoSetDirectDraw","SetDirectDraw","SetDirectDraw method [DirectShow]","SetDirectDraw method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::SetDirectDraw","dshow.idirectdrawvideo_setdirectdraw"]
old-location: dshow\idirectdrawvideo_setdirectdraw.htm
tech.root: dshow
ms.assetid: fd7b9571-2edb-4f36-b7a3-b280c37cb471
ms.date: 4/26/2023
ms.keywords: IDirectDrawVideo interface [DirectShow],SetDirectDraw method, IDirectDrawVideo.SetDirectDraw, IDirectDrawVideo::SetDirectDraw, IDirectDrawVideoSetDirectDraw, SetDirectDraw, SetDirectDraw method [DirectShow], SetDirectDraw method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::SetDirectDraw, dshow.idirectdrawvideo_setdirectdraw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawVideo::SetDirectDraw
 - amvideo/IDirectDrawVideo::SetDirectDraw
dev_langs:
 - c++
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
---

# IDirectDrawVideo::SetDirectDraw


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDirectDraw</code> method passes the <b>IDirectDraw</b> interface to a loaded driver.

## -parameters

### -param pDirectDraw

Pointer to the <b>IDirectDraw</b> interface to be passed.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

To have the renderer release a DirectDraw interface previously passed in through <code>SetDirectDraw</code>, an application can call <code>SetDirectDraw</code> and pass in <b>NULL</b>. However, the renderer will continue using that DirectDraw interface until it is disconnected. Therefore, calling <code>SetDirectDraw</code> with a <b>NULL</b> parameter does not make the renderer stop using it immediately.

This method was created because only one instance of <b>IDirectDraw</b> could be loaded per process in versions of DirectDraw prior to DirectX 7.0. If you are using DirectX 7.0 or later, you never need to call this method. If an application wanted to load <b>IDirectDraw</b> but allow the Video Renderer to also allocate surfaces, the application could open <b>IDirectDraw</b> itself and then pass the interface to the loaded driver through <code>IDirectDrawVideo::SetDirectDraw</code>. Alternatively, the application could let the renderer load DirectDraw and then obtain a reference-incremented interface to it through <a href="/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getdirectdraw">IDirectDrawVideo::GetDirectDraw</a>. Because DirectShow ships with the most recently shipped version of DirectDraw, however, this method is not required unless the application wants to change display modes itself and pass in a DirectDraw object, which the renderer can then use to allocate surfaces.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>