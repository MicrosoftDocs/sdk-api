---
UID: NF:mfmediaengine.IMFMediaEngine.GetDuration
title: IMFMediaEngine::GetDuration
author: windows-sdk-content
description: Gets the duration of the media resource.
old-location: mf\imfmediaengine_getduration.htm
old-project: medfound
ms.assetid: E5C793A2-7C6F-42D0-B8DE-17F1B62A0352
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetDuration, GetDuration method [Media Foundation], GetDuration method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetDuration method, IMFMediaEngine.GetDuration, IMFMediaEngine::GetDuration, mf.imfmediaengine_getduration, mfmediaengine/IMFMediaEngine::GetDuration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngine.GetDuration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::GetDuration


## -description


Gets the duration of the media resource.


## -parameters






## -returns



Returns the duration, in seconds. If no media data is available, the method returns not-a-number (NaN). If the duration is unbounded, the method returns an infinite value.




## -remarks



This method corresponds to the <b>duration</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If the duration changes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_DURATIONCHANGE</b> event. See <a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEngineNotify::EventNotify</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

