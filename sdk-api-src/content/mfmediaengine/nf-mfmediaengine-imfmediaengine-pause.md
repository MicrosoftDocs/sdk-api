---
UID: NF:mfmediaengine.IMFMediaEngine.Pause
title: IMFMediaEngine::Pause
author: windows-sdk-content
description: Pauses playback.
old-location: mf\imfmediaengine_pause.htm
tech.root: medfound
ms.assetid: 5C1FEBDA-18B5-4BF4-9AF4-FF6DBCDD880D
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],Pause method, IMFMediaEngine.Pause, IMFMediaEngine::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_pause, mfmediaengine/IMFMediaEngine::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfmediaengine.h
: 
- IMFMediaEngine.Pause
: 
---

# IMFMediaEngine::Pause


## -description


Pauses playback.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>pause</b> method of the <b>HTMLMediaElement</b> interface in HTML5.

The method completes asynchronously. When the transition to paused is complete, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_PAUSE                </b> event. See <a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEventNotify::EventNotify</a>.

Note that after you call <b>Pause</b>, the time returned by <a href="https://msdn.microsoft.com/49FA2383-8AEC-4DDF-8998-25987EEC8223">GetCurrentTime</a> may not be precisely accurate. Apps that need a frame-accurate position value, such as media editors, should call <a href="https://msdn.microsoft.com/090B5B6F-E4D1-43D7-AD09-BA3008B48104">FrameStep</a> immediately after calling **Pause** before calling <b>GetCurrentTime</b>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

