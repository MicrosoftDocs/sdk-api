---
UID: NF:control.IBasicVideo.get_VideoWidth
title: IBasicVideo::get_VideoWidth (control.h)
description: The get_VideoWidth method retrieves the native width of the video.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","get_VideoWidth method","IBasicVideo.get_VideoWidth","IBasicVideo::get_VideoWidth","IBasicVideoget_VideoWidth","control/IBasicVideo::get_VideoWidth","dshow.ibasicvideo_get_videowidth","get_VideoWidth","get_VideoWidth method [DirectShow]","get_VideoWidth method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_get_videowidth.htm
tech.root: dshow
ms.assetid: d5167b1e-1341-43b0-bc72-e990ee76e3c4
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],get_VideoWidth method, IBasicVideo.get_VideoWidth, IBasicVideo::get_VideoWidth, IBasicVideoget_VideoWidth, control/IBasicVideo::get_VideoWidth, dshow.ibasicvideo_get_videowidth, get_VideoWidth, get_VideoWidth method [DirectShow], get_VideoWidth method [DirectShow],IBasicVideo interface
req.header: control.h
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
 - IBasicVideo::get_VideoWidth
 - control/IBasicVideo::get_VideoWidth
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
 - IBasicVideo.get_VideoWidth
---

# IBasicVideo::get_VideoWidth


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The get_VideoWidth method retrieves the native width of the video.

## -parameters

### -param pVideoWidth [out]

Pointer to a variable that receives the width of the video, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>