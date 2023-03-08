---
UID: NN:mfidl.IMFQualityAdvise2
title: IMFQualityAdvise2 (mfidl.h)
description: Enables a pipeline object to adjust its own audio or video quality, in response to quality messages.
helpviewer_keywords: ["IMFQualityAdvise2","IMFQualityAdvise2 interface [Media Foundation]","IMFQualityAdvise2 interface [Media Foundation]","described","mf.imfqualityadvise2","mfidl/IMFQualityAdvise2"]
old-location: mf\imfqualityadvise2.htm
tech.root: mf
ms.assetid: c6114bbc-31d8-45eb-9bf8-745b3138dd50
ms.date: 12/05/2018
ms.keywords: IMFQualityAdvise2, IMFQualityAdvise2 interface [Media Foundation], IMFQualityAdvise2 interface [Media Foundation],described, mf.imfqualityadvise2, mfidl/IMFQualityAdvise2
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFQualityAdvise2
 - mfidl/IMFQualityAdvise2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFQualityAdvise2
---

# IMFQualityAdvise2 interface


## -description

Enables a pipeline object to adjust its own audio or video quality, in response to quality messages.

## -inheritance

The <b>IMFQualityAdvise2</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>. <b>IMFQualityAdvise2</b> also has these types of members:

## -remarks

This interface enables a pipeline object to respond to quality messages from the media sink. Currently, it is supported only for video decoders.

If a video decoder exposes <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a> but not <b>IMFQualityAdvise2</b>, the quality manager controls quality adjustments for the decoder. In this case, the quality manager responds to <a href="/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> events from the Enhanced Video Renderer (EVR) by calling <b>IMFQualityAdvise</b> methods on the decoder.

If the decoder exposes <b>IMFQualityAdvise2</b>, the quality manager forwards the <a href="/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> events to the decoder and does not adjust the decoder's quality settings. The decoder should respond to these events by adjusting its own quality settings internally.

The preceding remarks apply to the default implementation of the quality manager; custom quality managers can implement other behaviors.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
