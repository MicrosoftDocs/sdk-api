---
UID: NF:mfmediaengine.IMFMediaEngine.Play
title: IMFMediaEngine::Play
author: windows-sdk-content
description: Starts playback.
old-location: mf\imfmediaengine_play.htm
old-project: medfound
ms.assetid: 2D6083F5-734A-4350-8E54-56C79038389D
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],Play method, IMFMediaEngine.Play, IMFMediaEngine::Play, Play, Play method [Media Foundation], Play method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_play, mfmediaengine/IMFMediaEngine::Play
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.Play
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::Play


## -description


Starts playback.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>play</b> method of the <b>HTMLMediaElement</b> interface in HTML5.

The method completes asynchronously. When the operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_PLAY</b> event. When playback is under way, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_PLAYING</b> event. See <a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEventNotify::EventNotify</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

