---
UID: NF:amvideo.IFullScreenVideoEx.SetMessageDrain
title: IFullScreenVideoEx::SetMessageDrain (amvideo.h)
description: The SetMessageDrain method specifies a window to receive mouse and keyboard messages from the video window.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetMessageDrain method","IFullScreenVideoEx.SetMessageDrain","IFullScreenVideoEx::SetMessageDrain","IFullScreenVideoSetMessageDrain","SetMessageDrain","SetMessageDrain method [DirectShow]","SetMessageDrain method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetMessageDrain","dshow.ifullscreenvideoex_setmessagedrain"]
old-location: dshow\ifullscreenvideoex_setmessagedrain.htm
tech.root: dshow
ms.assetid: d0c24da9-c33f-48a7-b644-a7671acca20f
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetMessageDrain method, IFullScreenVideoEx.SetMessageDrain, IFullScreenVideoEx::SetMessageDrain, IFullScreenVideoSetMessageDrain, SetMessageDrain, SetMessageDrain method [DirectShow], SetMessageDrain method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetMessageDrain, dshow.ifullscreenvideoex_setmessagedrain
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
 - IFullScreenVideoEx::SetMessageDrain
 - amvideo/IFullScreenVideoEx::SetMessageDrain
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
 - IFullScreenVideoEx.SetMessageDrain
---

# IFullScreenVideoEx::SetMessageDrain


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetMessageDrain</code> method specifies a window to receive mouse and keyboard messages from the video window.

## -parameters

### -param hwnd [in]

Specifies a handle to the message-drain window.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method is equivalent to the <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_messagedrain">IVideoWindow::put_MessageDrain</a> method.

The Full Screen video renderer posts all mouse and keyboard messages to the window designated as a message drain. The exact list of messages that are posted is the same as the list given in <b>put_MessageDrain</b>.

Applications do not need to use this method. Instead, call the Filter Graph Manager's <b>put_MessageDrain</b> method before switching to full-screen mode. The Filter Graph Manager automatically sets the same message drain on the renderer that it selects for full-screen mode.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>