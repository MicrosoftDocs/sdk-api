---
UID: NF:strmif.IBPCSatelliteTuner.get_DefaultSubChannelTypes
title: IBPCSatelliteTuner::get_DefaultSubChannelTypes (strmif.h)
description: Note  The IBPCSatelliteTuner interface is deprecated. Gets the default sub-channel types.
helpviewer_keywords: ["IBPCSatelliteTuner interface [DirectShow]","get_DefaultSubChannelTypes method","IBPCSatelliteTuner.get_DefaultSubChannelTypes","IBPCSatelliteTuner::get_DefaultSubChannelTypes","IBPCSatelliteTunerget_DefaultSubChannelTypes","dshow.ibpcsatellitetuner_get_defaultsubchanneltypes","get_DefaultSubChannelTypes","get_DefaultSubChannelTypes method [DirectShow]","get_DefaultSubChannelTypes method [DirectShow]","IBPCSatelliteTuner interface","strmif/IBPCSatelliteTuner::get_DefaultSubChannelTypes"]
old-location: dshow\ibpcsatellitetuner_get_defaultsubchanneltypes.htm
tech.root: dshow
ms.assetid: 5e54b922-6018-4c6e-bf0d-4fba6640661c
ms.date: 4/26/2023
ms.keywords: IBPCSatelliteTuner interface [DirectShow],get_DefaultSubChannelTypes method, IBPCSatelliteTuner.get_DefaultSubChannelTypes, IBPCSatelliteTuner::get_DefaultSubChannelTypes, IBPCSatelliteTunerget_DefaultSubChannelTypes, dshow.ibpcsatellitetuner_get_defaultsubchanneltypes, get_DefaultSubChannelTypes, get_DefaultSubChannelTypes method [DirectShow], get_DefaultSubChannelTypes method [DirectShow],IBPCSatelliteTuner interface, strmif/IBPCSatelliteTuner::get_DefaultSubChannelTypes
req.header: strmif.h
req.include-header: Dshow.h
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
 - IBPCSatelliteTuner::get_DefaultSubChannelTypes
 - strmif/IBPCSatelliteTuner::get_DefaultSubChannelTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IBPCSatelliteTuner.get_DefaultSubChannelTypes
---

# IBPCSatelliteTuner::get_DefaultSubChannelTypes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IBPCSatelliteTuner</b> interface is deprecated.</div>
<div> </div>
Gets the default sub-channel types.

## -parameters

### -param plDefaultVideoType [out]

Receives a provider-specific service type for video.

### -param plDefaultAudioType [out]

Receives a provider-specific service type for audio.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ibpcsatellitetuner">IBPCSatelliteTuner Interface</a>