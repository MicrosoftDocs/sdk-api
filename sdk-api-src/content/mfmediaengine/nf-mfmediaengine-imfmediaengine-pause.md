---
UID: NF:mfmediaengine.IMFMediaEngine.Pause
title: IMFMediaEngine::Pause (mfmediaengine.h)
description: Pauses playback.helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","Pause method","IMFMediaEngine.Pause","IMFMediaEngine::Pause","Pause","Pause method [Media Foundation]","Pause method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_pause","mfmediaengine/IMFMediaEngine::Pause"]
old-location: mf\imfmediaengine_pause.htm
tech.root: medfound
ms.assetid: 5C1FEBDA-18B5-4BF4-9AF4-FF6DBCDD880D
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],Pause method, IMFMediaEngine.Pause, IMFMediaEngine::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_pause, mfmediaengine/IMFMediaEngine::Pause
f1_keywords:
- mfmediaengine/IMFMediaEngine.Pause
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
- IMFMediaEngine.Pause
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine::Pause


## -description


Pauses playback.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>pause</b> method of the <b>HTMLMediaElement</b> interface in HTML5.

The method completes asynchronously. When the transition to paused is complete, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_PAUSE                </b> event. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEventNotify::EventNotify</a>.

Note that after you call <b>Pause</b>, the time returned by <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getcurrenttime">GetCurrentTime</a> may not be precisely accurate. Apps that need a frame-accurate position value, such as media editors, should call <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-framestep">FrameStep</a> immediately after calling **Pause** before calling <b>GetCurrentTime</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
 

 

