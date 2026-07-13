---
UID: NN:strmif.IDrawVideoImage
title: IDrawVideoImage (strmif.h)
description: Note  This interface has been deprecated. (IDrawVideoImage)
helpviewer_keywords: ["IDrawVideoImage","IDrawVideoImage interface [DirectShow]","IDrawVideoImage interface [DirectShow]","described","IDrawVideoImageInterface","dshow.idrawvideoimage","strmif/IDrawVideoImage"]
old-location: dshow\idrawvideoimage.htm
tech.root: dshow
ms.assetid: ff412213-60e5-43d8-8cb1-e7ae8b3ca1bc
ms.date: 4/26/2023
ms.keywords: IDrawVideoImage, IDrawVideoImage interface [DirectShow], IDrawVideoImage interface [DirectShow],described, IDrawVideoImageInterface, dshow.idrawvideoimage, strmif/IDrawVideoImage
req.header: strmif.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDrawVideoImage
 - strmif/IDrawVideoImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IDrawVideoImage
---

# IDrawVideoImage interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDrawVideoImage</code> interface enables an application to draw the same video image in multiple places simultaneously on the screen. The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter exposes this interface. The Video Mixing Renderer (VMR) filter provides a better way to accomplish the same effect, through the use of multiple input streams.

To use this interface, call <b>DrawVideoImageBegin</b> to put the Video Renderer into GDI mode. Then the application can call the <b>DrawVideoImageDraw</b> method as often as necessary. The renderer simply takes the current video frame and draws it to the specified rectangle. This process is asynchronous to the delivery of frames to the renderer on the filter graph thread. The application is responsible for the frame rate at which it renders images; this rate will never be the same as the rate of the frames being delivered to the filter. In other words, calling this method is like taking a periodic snapshot of the video and putting it into a device context of your choosing at a rate of your choosing.

## -inheritance

The <b>IDrawVideoImage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDrawVideoImage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
