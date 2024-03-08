---
UID: NF:amvideo.IDirectDrawVideo.UseOverlayStretch
title: IDirectDrawVideo::UseOverlayStretch (amvideo.h)
description: The UseOverlayStretch method determines whether the renderer should check overlay stretch limitations.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","UseOverlayStretch method","IDirectDrawVideo.UseOverlayStretch","IDirectDrawVideo::UseOverlayStretch","IDirectDrawVideoUseOverlayStretch","UseOverlayStretch","UseOverlayStretch method [DirectShow]","UseOverlayStretch method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::UseOverlayStretch","dshow.idirectdrawvideo_useoverlaystretch"]
old-location: dshow\idirectdrawvideo_useoverlaystretch.htm
tech.root: dshow
ms.assetid: e617b40d-ba5b-4fc8-825e-3c751f72bc2c
ms.date: 4/26/2023
ms.keywords: IDirectDrawVideo interface [DirectShow],UseOverlayStretch method, IDirectDrawVideo.UseOverlayStretch, IDirectDrawVideo::UseOverlayStretch, IDirectDrawVideoUseOverlayStretch, UseOverlayStretch, UseOverlayStretch method [DirectShow], UseOverlayStretch method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::UseOverlayStretch, dshow.idirectdrawvideo_useoverlaystretch
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
 - IDirectDrawVideo::UseOverlayStretch
 - amvideo/IDirectDrawVideo::UseOverlayStretch
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
 - IDirectDrawVideo.UseOverlayStretch
---

# IDirectDrawVideo::UseOverlayStretch


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UseOverlayStretch</code> method determines whether the renderer should check overlay stretch limitations.

## -parameters

### -param UseOverlayStretch

Value specifying whether the renderer checks overlay stretching. Set to OATRUE for the renderer to check overlay stretching; otherwise, set to OAFALSE.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Some display cards provide the use of overlay surfaces through DirectDraw. An overlay surface is a block of video memory whose contents are overlaid onto the display during the monitor's vertical refresh. DirectShow uses all available overlay surfaces where possible because they typically offer higher-quality video and very fast performance. On some display cards set to relatively high bit depths, the overlay must be displayed on the screen larger than its real size (to accommodate certain display hardware bandwidth limitations). If the overlay is not displayed large enough, certain undesirable effects can be seen on the display (sometimes described as a "fleeting shimmering" effect).

If <i>UseOverlayStretch</i> is set to OATRUE (on, the default), DirectShow will ensure the overlay is adequately stretched before displaying it. If it is set to OAFALSE (off), DirectShow will not check that the overlay is adequately stretched, and the user is likely to experience artifacts on the screen (although it will also guarantee that the overlay will be used if possible).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>