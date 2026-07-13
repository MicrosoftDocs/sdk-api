---
UID: NN:strmif.IDecimateVideoImage
title: IDecimateVideoImage (strmif.h)
description: The IDecimateVideoImage interface specifies decimation on a decoder filter.
helpviewer_keywords: ["IDecimateVideoImage","IDecimateVideoImage interface [DirectShow]","IDecimateVideoImage interface [DirectShow]","described","IDecimateVideoImageInterface","dshow.idecimatevideoimage","strmif/IDecimateVideoImage"]
old-location: dshow\idecimatevideoimage.htm
tech.root: dshow
ms.assetid: 0d338d41-546f-41da-bc1f-b1dd74b399ef
ms.date: 4/26/2023
ms.keywords: IDecimateVideoImage, IDecimateVideoImage interface [DirectShow], IDecimateVideoImage interface [DirectShow],described, IDecimateVideoImageInterface, dshow.idecimatevideoimage, strmif/IDecimateVideoImage
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDecimateVideoImage
 - strmif/IDecimateVideoImage
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
 - IDecimateVideoImage
---

# IDecimateVideoImage interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDecimateVideoImage</code> interface specifies decimation on a decoder filter. The term <i>decimation</i> refers to scaling the video output down to a size smaller than the native size of the video.

Applications must not call methods on this interface. The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter uses this interface to decimate video at the video decoder.

Decoder filters that can decimate their video output should support this interface.

## -inheritance

The <b>IDecimateVideoImage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDecimateVideoImage</b> also has these types of members:

