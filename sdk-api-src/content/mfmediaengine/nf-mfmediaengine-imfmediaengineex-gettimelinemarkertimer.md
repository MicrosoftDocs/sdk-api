---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetTimelineMarkerTimer
title: IMFMediaEngineEx::GetTimelineMarkerTimer (mfmediaengine.h)
description: Gets the time of the next timeline marker, if any.
helpviewer_keywords: ["GetTimelineMarkerTimer","GetTimelineMarkerTimer method [Media Foundation]","GetTimelineMarkerTimer method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetTimelineMarkerTimer method","IMFMediaEngineEx.GetTimelineMarkerTimer","IMFMediaEngineEx::GetTimelineMarkerTimer","mf.imfmediaengineex_gettimelinemarkertimer","mfmediaengine/IMFMediaEngineEx::GetTimelineMarkerTimer"]
old-location: mf\imfmediaengineex_gettimelinemarkertimer.htm
tech.root: mf
ms.assetid: 8C58DBB6-A55E-4992-B4F2-EB36E15FA7A1
ms.date: 12/05/2018
ms.keywords: GetTimelineMarkerTimer, GetTimelineMarkerTimer method [Media Foundation], GetTimelineMarkerTimer method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetTimelineMarkerTimer method, IMFMediaEngineEx.GetTimelineMarkerTimer, IMFMediaEngineEx::GetTimelineMarkerTimer, mf.imfmediaengineex_gettimelinemarkertimer, mfmediaengine/IMFMediaEngineEx::GetTimelineMarkerTimer
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
 - IMFMediaEngineEx::GetTimelineMarkerTimer
 - mfmediaengine/IMFMediaEngineEx::GetTimelineMarkerTimer
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
 - IMFMediaEngineEx.GetTimelineMarkerTimer
---

# IMFMediaEngineEx::GetTimelineMarkerTimer


## -description

Gets the time of the next timeline marker, if any.

## -parameters

### -param pTimeToFire [out]

Receives the marker time, in seconds. If no marker is set, this parameter receives the value <b>NaN</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>