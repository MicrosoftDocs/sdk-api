---
UID: NF:strmif.IBPCSatelliteTuner.IsTapingPermitted
title: IBPCSatelliteTuner::IsTapingPermitted (strmif.h)
description: Note  The IBPCSatelliteTuner interface is deprecated. Queries whether taping is permitted.
helpviewer_keywords: ["IBPCSatelliteTuner interface [DirectShow]","IsTapingPermitted method","IBPCSatelliteTuner.IsTapingPermitted","IBPCSatelliteTuner::IsTapingPermitted","IBPCSatelliteTunerIsTapingPermitted","IsTapingPermitted","IsTapingPermitted method [DirectShow]","IsTapingPermitted method [DirectShow]","IBPCSatelliteTuner interface","dshow.ibpcsatellitetuner_istapingpermitted","strmif/IBPCSatelliteTuner::IsTapingPermitted"]
old-location: dshow\ibpcsatellitetuner_istapingpermitted.htm
tech.root: dshow
ms.assetid: 5e5b661f-46d5-47f1-adeb-d323c57ddff0
ms.date: 4/26/2023
ms.keywords: IBPCSatelliteTuner interface [DirectShow],IsTapingPermitted method, IBPCSatelliteTuner.IsTapingPermitted, IBPCSatelliteTuner::IsTapingPermitted, IBPCSatelliteTunerIsTapingPermitted, IsTapingPermitted, IsTapingPermitted method [DirectShow], IsTapingPermitted method [DirectShow],IBPCSatelliteTuner interface, dshow.ibpcsatellitetuner_istapingpermitted, strmif/IBPCSatelliteTuner::IsTapingPermitted
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
 - IBPCSatelliteTuner::IsTapingPermitted
 - strmif/IBPCSatelliteTuner::IsTapingPermitted
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
 - IBPCSatelliteTuner.IsTapingPermitted
---

# IBPCSatelliteTuner::IsTapingPermitted


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IBPCSatelliteTuner</b> interface is deprecated.</div>
<div> </div>
Queries whether taping is permitted.



## -returns

Returns S_OK if taping is permitted or S_FALSE if taping is not permitted.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ibpcsatellitetuner">IBPCSatelliteTuner Interface</a>
