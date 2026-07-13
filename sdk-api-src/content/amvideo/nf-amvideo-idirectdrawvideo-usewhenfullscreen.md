---
UID: NF:amvideo.IDirectDrawVideo.UseWhenFullScreen
title: IDirectDrawVideo::UseWhenFullScreen (amvideo.h)
description: The UseWhenFullScreen method determines whether DirectShow should change display mode when going to full-screen mode.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","UseWhenFullScreen method","IDirectDrawVideo.UseWhenFullScreen","IDirectDrawVideo::UseWhenFullScreen","IDirectDrawVideoUseWhenFullScreen","UseWhenFullScreen","UseWhenFullScreen method [DirectShow]","UseWhenFullScreen method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::UseWhenFullScreen","dshow.idirectdrawvideo_usewhenfullscreen"]
old-location: dshow\idirectdrawvideo_usewhenfullscreen.htm
tech.root: dshow
ms.assetid: e50f7f06-6534-4373-a2b8-fa315158729d
ms.date: 4/26/2023
ms.keywords: IDirectDrawVideo interface [DirectShow],UseWhenFullScreen method, IDirectDrawVideo.UseWhenFullScreen, IDirectDrawVideo::UseWhenFullScreen, IDirectDrawVideoUseWhenFullScreen, UseWhenFullScreen, UseWhenFullScreen method [DirectShow], UseWhenFullScreen method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::UseWhenFullScreen, dshow.idirectdrawvideo_usewhenfullscreen
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
 - IDirectDrawVideo::UseWhenFullScreen
 - amvideo/IDirectDrawVideo::UseWhenFullScreen
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
 - IDirectDrawVideo.UseWhenFullScreen
---

# IDirectDrawVideo::UseWhenFullScreen


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UseWhenFullScreen</code> method determines whether DirectShow should change display mode when going to full-screen mode.

## -parameters

### -param UseWhenFullScreen

Value specifying whether to change the display mode. Set to OATRUE to cause the renderer to use DirectShow in full-screen mode; otherwise, set to OAFALSE.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

When asked to go to full-screen mode, DirectShow has a number of choices. The first choice is to determine if any filters in the graph can support full-screen playback directly; if one can, it will be asked to do so.

The second choice is to automatically add a special full-screen renderer to the filter graph that uses DirectDraw mode-changing services to play back the video. By changing display modes, the video effectively fills more (but not necessarily all) of the display. So, for example, if the current mode is 1024 x 768 pixels, a video might look relatively small, but when displayed in a 320 x 240 display mode it might look very presentable.

The third and final choice is to simply take any renderer supporting the <a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow</a> interface and have its window stretched full-screen. This will typically offer lower performance than the second option (swapping in a full-screen DirectDraw-enabled renderer). If the <i>UseWhenFullScreen</i> parameter is set to On (OATRUE), the window will always be stretched full-screen for full-screen playback; if set to Off (the default), the filter graph manager is free to swap in the DirectDraw-enabled full-screen renderer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>