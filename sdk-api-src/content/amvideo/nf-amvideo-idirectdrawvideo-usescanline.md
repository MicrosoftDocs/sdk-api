---
UID: NF:amvideo.IDirectDrawVideo.UseScanLine
title: IDirectDrawVideo::UseScanLine (amvideo.h)
description: The UseScanLine method determines whether the renderer should check the current scan line when drawing a video.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","UseScanLine method","IDirectDrawVideo.UseScanLine","IDirectDrawVideo::UseScanLine","IDirectDrawVideoUseScanLine","UseScanLine","UseScanLine method [DirectShow]","UseScanLine method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::UseScanLine","dshow.idirectdrawvideo_usescanline"]
old-location: dshow\idirectdrawvideo_usescanline.htm
tech.root: dshow
ms.assetid: 8378582d-ef82-47ff-a801-934c900ac328
ms.date: 4/26/2023
ms.keywords: IDirectDrawVideo interface [DirectShow],UseScanLine method, IDirectDrawVideo.UseScanLine, IDirectDrawVideo::UseScanLine, IDirectDrawVideoUseScanLine, UseScanLine, UseScanLine method [DirectShow], UseScanLine method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::UseScanLine, dshow.idirectdrawvideo_usescanline
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
 - IDirectDrawVideo::UseScanLine
 - amvideo/IDirectDrawVideo::UseScanLine
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
 - IDirectDrawVideo.UseScanLine
---

# IDirectDrawVideo::UseScanLine


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UseScanLine</code> method determines whether the renderer should check the current scan line when drawing a video.

## -parameters

### -param UseScanLine

Long integer value that specifies whether or not to use the scan line information. Set to <b>OATRUE</b> to use scan line information or <b>OAFALSE</b> to ignore it.

## -returns

Returns E_INVALIDARG if the argument is invalid or S_OK otherwise.

## -remarks

If you blit an image to the video memory while the monitor's scan line is scanning over a visible portion of the screen, the complete image will be a composite of the old and new images. This composite is known as a torn video image. You can avoid torn images by waiting until the previous image is complete before blitting the new image. Some video cards can retrieve the scan line's current position; if this information is available, you can have DirectShow try to reduce tearing by waiting until the scan line is off-screen before blitting the new image. Note that checking the scan line location increases load on the processor and can reduce the amount of video frames delivered to the screen. If scan line information is available, DirectShow uses it by default. Set <i>UseScanLine</i> to OAFALSE if you want to save processing time at the expense of minor image degradation.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>