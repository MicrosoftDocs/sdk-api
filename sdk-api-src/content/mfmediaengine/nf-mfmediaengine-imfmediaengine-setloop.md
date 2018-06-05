---
UID: NF:mfmediaengine.IMFMediaEngine.SetLoop
title: IMFMediaEngine::SetLoop
author: windows-sdk-content
description: Specifies whether the Media Engine loops playback.
old-location: mf\imfmediaengine_setloop.htm
old-project: medfound
ms.assetid: 0B8890EA-9207-428B-8EC2-18B51E1D8365
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetLoop method, IMFMediaEngine.SetLoop, IMFMediaEngine::SetLoop, SetLoop, SetLoop method [Media Foundation], SetLoop method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setloop, mfmediaengine/IMFMediaEngine::SetLoop
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
tech.root: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngine.SetLoop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::SetLoop


## -description


Specifies whether the Media Engine loops playback.


## -parameters




### -param Loop [in]

Specify <b>TRUE</b> to enable looping, or <b>FALSE</b> to disable looping.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>Loop</i> is <b>TRUE</b>, playback loops back to the beginning when it reaches the end of the source.

This method corresponds to setting the <b>loop</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

