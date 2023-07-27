---
UID: NF:amvideo.IDirectDrawVideo.WillUseFullScreen
title: IDirectDrawVideo::WillUseFullScreen (amvideo.h)
description: The WillUseFullScreen method determines whether DirectShow will change display mode when going to full-screen mode.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","WillUseFullScreen method","IDirectDrawVideo.WillUseFullScreen","IDirectDrawVideo::WillUseFullScreen","IDirectDrawVideoWillUseFullScreen","WillUseFullScreen","WillUseFullScreen method [DirectShow]","WillUseFullScreen method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::WillUseFullScreen","dshow.idirectdrawvideo_willusefullscreen"]
old-location: dshow\idirectdrawvideo_willusefullscreen.htm
tech.root: dshow
ms.assetid: de2addfc-e289-4277-a283-b7aa2aa47ba0
ms.date: 4/26/2023
ms.keywords: IDirectDrawVideo interface [DirectShow],WillUseFullScreen method, IDirectDrawVideo.WillUseFullScreen, IDirectDrawVideo::WillUseFullScreen, IDirectDrawVideoWillUseFullScreen, WillUseFullScreen, WillUseFullScreen method [DirectShow], WillUseFullScreen method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::WillUseFullScreen, dshow.idirectdrawvideo_willusefullscreen
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
 - IDirectDrawVideo::WillUseFullScreen
 - amvideo/IDirectDrawVideo::WillUseFullScreen
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
 - IDirectDrawVideo.WillUseFullScreen
---

# IDirectDrawVideo::WillUseFullScreen


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>WillUseFullScreen</code> method determines whether DirectShow will change display mode when going to full-screen mode.

## -parameters

### -param UseWhenFullScreen

Pointer to a value indicating whether DirectShow will use DirectX in full-screen mode. OATRUE indicates it will use full-screen mode; OAFALSE indicates it will not.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

For a description of this feature, see <a href="/previous-versions/ms785118(v=vs.85)">IDirectDrawVideo::UseWhenFullScreen</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>