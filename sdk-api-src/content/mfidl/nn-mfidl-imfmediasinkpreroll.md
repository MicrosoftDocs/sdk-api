---
UID: NN:mfidl.IMFMediaSinkPreroll
title: IMFMediaSinkPreroll (mfidl.h)
description: Enables a media sink to receive samples before the presentation clock is started.
helpviewer_keywords: ["7cc93751-4477-4649-b09e-53f519fb1acb","IMFMediaSinkPreroll","IMFMediaSinkPreroll interface [Media Foundation]","IMFMediaSinkPreroll interface [Media Foundation]","described","mf.imfmediasinkpreroll","mfidl/IMFMediaSinkPreroll"]
old-location: mf\imfmediasinkpreroll.htm
tech.root: mf
ms.assetid: 7cc93751-4477-4649-b09e-53f519fb1acb
ms.date: 12/05/2018
ms.keywords: 7cc93751-4477-4649-b09e-53f519fb1acb, IMFMediaSinkPreroll, IMFMediaSinkPreroll interface [Media Foundation], IMFMediaSinkPreroll interface [Media Foundation],described, mf.imfmediasinkpreroll, mfidl/IMFMediaSinkPreroll
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSinkPreroll
 - mfidl/IMFMediaSinkPreroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSinkPreroll
---

# IMFMediaSinkPreroll interface


## -description

Enables a media sink to receive samples before the presentation clock is started.

To get a pointer to this interface, call <b>QueryInterface</b> on the media sink.

## -inheritance

The <b>IMFMediaSinkPreroll</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSinkPreroll</b> also has these types of members:

## -remarks

Media sinks can implement this interface to support seamless playback and transitions. If a media sink exposes this interface, it can receive samples before the presentation clock starts. It can then pre-process the samples, so that rendering can begin immediately when the clock starts. Prerolling helps to avoid glitches during playback.

If a media sink supports preroll, the media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics">IMFMediaSink::GetCharacteristics</a> method should return the MEDIASINK_CAN_PREROLL flag.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>
