---
UID: NF:mfmediaengine.IMFMediaEngine.GetDuration
title: IMFMediaEngine::GetDuration (mfmediaengine.h)
description: Gets the duration of the media resource.helpviewer_keywords: ["GetDuration","GetDuration method [Media Foundation]","GetDuration method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetDuration method","IMFMediaEngine.GetDuration","IMFMediaEngine::GetDuration","mf.imfmediaengine_getduration","mfmediaengine/IMFMediaEngine::GetDuration"]
old-location: mf\imfmediaengine_getduration.htm
tech.root: medfound
ms.assetid: E5C793A2-7C6F-42D0-B8DE-17F1B62A0352
ms.date: 12/05/2018
ms.keywords: GetDuration, GetDuration method [Media Foundation], GetDuration method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetDuration method, IMFMediaEngine.GetDuration, IMFMediaEngine::GetDuration, mf.imfmediaengine_getduration, mfmediaengine/IMFMediaEngine::GetDuration
f1_keywords:
- mfmediaengine/IMFMediaEngine.GetDuration
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFMediaEngine.GetDuration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine::GetDuration


## -description


Gets the duration of the media resource.


## -parameters






## -returns



Returns the duration, in seconds. If no media data is available, the method returns not-a-number (NaN). If the duration is unbounded, the method returns an infinite value.




## -remarks



This method corresponds to the <b>duration</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If the duration changes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_DURATIONCHANGE</b> event. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEngineNotify::EventNotify</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
 

 

