---
UID: NF:strmif.IBPCSatelliteTuner.put_DefaultSubChannelTypes
title: IBPCSatelliteTuner::put_DefaultSubChannelTypes (strmif.h)
description: Note  The IBPCSatelliteTuner interface is deprecated. Sets the default sub-channel types.
helpviewer_keywords: ["IBPCSatelliteTuner interface [DirectShow]","put_DefaultSubChannelTypes method","IBPCSatelliteTuner.put_DefaultSubChannelTypes","IBPCSatelliteTuner::put_DefaultSubChannelTypes","IBPCSatelliteTunerput_DefaultSubChannelTypes","dshow.ibpcsatellitetuner_put_defaultsubchanneltypes","put_DefaultSubChannelTypes","put_DefaultSubChannelTypes method [DirectShow]","put_DefaultSubChannelTypes method [DirectShow]","IBPCSatelliteTuner interface","strmif/IBPCSatelliteTuner::put_DefaultSubChannelTypes"]
old-location: dshow\ibpcsatellitetuner_put_defaultsubchanneltypes.htm
tech.root: dshow
ms.assetid: 90f73ca0-1d9a-4161-bc86-d69cc71e88c6
ms.date: 4/26/2023
ms.keywords: IBPCSatelliteTuner interface [DirectShow],put_DefaultSubChannelTypes method, IBPCSatelliteTuner.put_DefaultSubChannelTypes, IBPCSatelliteTuner::put_DefaultSubChannelTypes, IBPCSatelliteTunerput_DefaultSubChannelTypes, dshow.ibpcsatellitetuner_put_defaultsubchanneltypes, put_DefaultSubChannelTypes, put_DefaultSubChannelTypes method [DirectShow], put_DefaultSubChannelTypes method [DirectShow],IBPCSatelliteTuner interface, strmif/IBPCSatelliteTuner::put_DefaultSubChannelTypes
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
 - IBPCSatelliteTuner::put_DefaultSubChannelTypes
 - strmif/IBPCSatelliteTuner::put_DefaultSubChannelTypes
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
 - IBPCSatelliteTuner.put_DefaultSubChannelTypes
---

# IBPCSatelliteTuner::put_DefaultSubChannelTypes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <code>IBPCSatelliteTuner</code> interface is deprecated.</div>
<div> </div>
Sets the default sub-channel types.

## -parameters

### -param lDefaultVideoType [in]

Provider-specific service type for video.

### -param lDefaultAudioType [in]

Provider-specific service type for audio.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ibpcsatellitetuner">IBPCSatelliteTuner Interface</a>