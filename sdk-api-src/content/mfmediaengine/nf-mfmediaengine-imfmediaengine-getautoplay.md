---
UID: NF:mfmediaengine.IMFMediaEngine.GetAutoPlay
title: IMFMediaEngine::GetAutoPlay
author: windows-sdk-content
description: Queries whether the Media Engine automatically begins playback.
old-location: mf\imfmediaengine_getautoplay.htm
tech.root: medfound
ms.assetid: CEF50308-D4F9-435F-A81A-3746A27846F0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetAutoPlay, GetAutoPlay method [Media Foundation], GetAutoPlay method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetAutoPlay method, IMFMediaEngine.GetAutoPlay, IMFMediaEngine::GetAutoPlay, mf.imfmediaengine_getautoplay, mfmediaengine/IMFMediaEngine::GetAutoPlay
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
 - IMFMediaEngine.GetAutoPlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::GetAutoPlay


## -description


Queries whether the Media Engine automatically begins playback.


## -parameters






## -returns



Returns <b>TRUE</b> if the Media Engine automatically begins playback, or <b>FALSE</b> otherwise.




## -remarks



This method corresponds to the <b>autoplay</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If this method returns <b>TRUE</b>, playback begins automatically after the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">IMFMediaEngine::Load</a> method completes. Otherwise, playback begins when the application calls <a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">IMFMediaEngine::Play</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>



<a href="https://msdn.microsoft.com/867FE1D2-39AE-4A44-99DD-98A8ABD234A2">IMFMediaEngine::SetAutoPlay</a>
 

 

