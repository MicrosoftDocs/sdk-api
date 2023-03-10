---
UID: NF:mfmediaengine.IMFMediaEngineEx.IsPlaybackRateSupported
title: IMFMediaEngineEx::IsPlaybackRateSupported (mfmediaengine.h)
description: Queries whether the Media Engine can play at a specified playback rate.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","IsPlaybackRateSupported method","IMFMediaEngineEx.IsPlaybackRateSupported","IMFMediaEngineEx::IsPlaybackRateSupported","IsPlaybackRateSupported","IsPlaybackRateSupported method [Media Foundation]","IsPlaybackRateSupported method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_isplaybackratesupported","mfmediaengine/IMFMediaEngineEx::IsPlaybackRateSupported"]
old-location: mf\imfmediaengineex_isplaybackratesupported.htm
tech.root: mf
ms.assetid: 2BE9954A-0B67-45A8-9B79-1148DCB4DDC4
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],IsPlaybackRateSupported method, IMFMediaEngineEx.IsPlaybackRateSupported, IMFMediaEngineEx::IsPlaybackRateSupported, IsPlaybackRateSupported, IsPlaybackRateSupported method [Media Foundation], IsPlaybackRateSupported method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_isplaybackratesupported, mfmediaengine/IMFMediaEngineEx::IsPlaybackRateSupported
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::IsPlaybackRateSupported
 - mfmediaengine/IMFMediaEngineEx::IsPlaybackRateSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.IsPlaybackRateSupported
---

# IMFMediaEngineEx::IsPlaybackRateSupported


## -description

Queries whether the Media Engine can play at a specified playback rate.

## -parameters

### -param rate [in]

The requested playback rate.

## -returns

Returns <b>TRUE</b> if the playback rate is supported, or <b>FALSE</b> otherwise.

## -remarks

Playback rates are expressed as a ratio of the current rate to the normal rate. For example, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is 2× speed. Positive values mean forward playback, and negative values mean reverse playback.

The results of this method can vary depending on the media resource that is currently loaded. Some media formats might support faster playback rates than others. Also, some formats might not support reverse play.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>