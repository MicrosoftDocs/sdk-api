---
UID: NF:mfmediaengine.IMFMediaEngine.GetCurrentTime
title: IMFMediaEngine::GetCurrentTime
author: windows-sdk-content
description: Gets the current playback position.
old-location: mf\imfmediaengine_getcurrenttime.htm
tech.root: medfound
ms.assetid: 49FA2383-8AEC-4DDF-8998-25987EEC8223
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetCurrentTime, GetCurrentTime method [Media Foundation], GetCurrentTime method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetCurrentTime method, IMFMediaEngine.GetCurrentTime, IMFMediaEngine::GetCurrentTime, mf.imfmediaengine_getcurrenttime, mfmediaengine/IMFMediaEngine::GetCurrentTime
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
 - IMFMediaEngine.GetCurrentTime
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
- IMFMediaEngine.GetCurrentTime
: 
---

# IMFMediaEngine::GetCurrentTime


## -description


Gets the current playback position.


## -parameters






## -returns



Returns the playback position, in seconds.




## -remarks



This method corresponds to the <b>currentTime</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. 

Note that after you call <a href="https://msdn.microsoft.com/5C1FEBDA-18B5-4BF4-9AF4-FF6DBCDD880D">Pause</a>, the time returned by <b>GetCurrentTime</b> may not be precisely accurate. Apps that need a frame-accurate position value, such as media editors, should call <a href="https://msdn.microsoft.com/090B5B6F-E4D1-43D7-AD09-BA3008B48104">FrameStep</a> immediately after calling **Pause** before calling <b>GetCurrentTime</b>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

