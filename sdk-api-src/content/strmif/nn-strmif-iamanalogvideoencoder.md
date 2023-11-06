---
UID: NN:strmif.IAMAnalogVideoEncoder
title: IAMAnalogVideoEncoder (strmif.h)
description: Note  This interface has been deprecated. Note  Microsoft does not provide an implementation of this interface.
helpviewer_keywords: ["IAMAnalogVideoEncoder","IAMAnalogVideoEncoder interface [DirectShow]","IAMAnalogVideoEncoder interface [DirectShow]","described","IAMAnalogVideoEncoderInterface","dshow.iamanalogvideoencoder","strmif/IAMAnalogVideoEncoder"]
old-location: dshow\iamanalogvideoencoder.htm
tech.root: dshow
ms.assetid: fb2927cf-c979-411f-a896-d010b684acf2
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoEncoder, IAMAnalogVideoEncoder interface [DirectShow], IAMAnalogVideoEncoder interface [DirectShow],described, IAMAnalogVideoEncoderInterface, dshow.iamanalogvideoencoder, strmif/IAMAnalogVideoEncoder
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
 - IAMAnalogVideoEncoder
 - strmif/IAMAnalogVideoEncoder
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
 - IAMAnalogVideoEncoder
---

# IAMAnalogVideoEncoder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated.</div>
<div> </div>
<div class="alert"><b>Note</b>  Microsoft does not provide an implementation of this interface. Third parties might implement it.</div>
<div> </div>
The <b>IAMAnalogVideoEncoder</b> interface might be implemented by a hardware video encoder in video capture operations when an application is streaming data to disk and sending it back out to videotape.

## -inheritance

The <b>IAMAnalogVideoEncoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAnalogVideoEncoder</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
