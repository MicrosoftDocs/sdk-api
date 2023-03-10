---
UID: NF:mfmediaengine.IMFMediaEngineEx.CancelTimelineMarkerTimer
title: IMFMediaEngineEx::CancelTimelineMarkerTimer (mfmediaengine.h)
description: Cancels the next pending timeline marker.
helpviewer_keywords: ["CancelTimelineMarkerTimer","CancelTimelineMarkerTimer method [Media Foundation]","CancelTimelineMarkerTimer method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","CancelTimelineMarkerTimer method","IMFMediaEngineEx.CancelTimelineMarkerTimer","IMFMediaEngineEx::CancelTimelineMarkerTimer","mf.imfmediaengineex_canceltimelinemarkertimer","mfmediaengine/IMFMediaEngineEx::CancelTimelineMarkerTimer"]
old-location: mf\imfmediaengineex_canceltimelinemarkertimer.htm
tech.root: mf
ms.assetid: AC295919-747B-445D-8C74-E648A612C0BF
ms.date: 12/05/2018
ms.keywords: CancelTimelineMarkerTimer, CancelTimelineMarkerTimer method [Media Foundation], CancelTimelineMarkerTimer method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],CancelTimelineMarkerTimer method, IMFMediaEngineEx.CancelTimelineMarkerTimer, IMFMediaEngineEx::CancelTimelineMarkerTimer, mf.imfmediaengineex_canceltimelinemarkertimer, mfmediaengine/IMFMediaEngineEx::CancelTimelineMarkerTimer
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
 - IMFMediaEngineEx::CancelTimelineMarkerTimer
 - mfmediaengine/IMFMediaEngineEx::CancelTimelineMarkerTimer
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
 - IMFMediaEngineEx.CancelTimelineMarkerTimer
---

# IMFMediaEngineEx::CancelTimelineMarkerTimer


## -description

Cancels the next pending timeline marker.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method to cancel the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-settimelinemarkertimer">IMFMediaEngineEx::SetTimelineMarkerTimer</a> method.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
