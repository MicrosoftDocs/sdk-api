---
UID: NF:mfmediaengine.IMFMediaEngine.GetLoop
title: IMFMediaEngine::GetLoop
author: windows-sdk-content
description: Queries whether the Media Engine will loop playback.
old-location: mf\imfmediaengine_getloop.htm
tech.root: medfound
ms.assetid: EBAB4E73-164D-4AE5-87A4-0D37C10071E9
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetLoop, GetLoop method [Media Foundation], GetLoop method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetLoop method, IMFMediaEngine.GetLoop, IMFMediaEngine::GetLoop, mf.imfmediaengine_getloop, mfmediaengine/IMFMediaEngine::GetLoop
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
 - IMFMediaEngine.GetLoop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::GetLoop


## -description


Queries whether the Media Engine will loop playback.


## -parameters






## -returns



Returns <b>TRUE</b> if looping is enabled, or <b>FALSE</b> otherwise.




## -remarks



This method corresponds to getting the <b>loop</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If looping is enabled, the Media Engine seeks to the start of the content when playback reaches the end.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

