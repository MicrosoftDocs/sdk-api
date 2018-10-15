---
UID: NF:mfmediaengine.IMFMediaEngine.GetSeekable
title: IMFMediaEngine::GetSeekable
author: windows-sdk-content
description: Gets the time ranges to which the Media Engine can currently seek.
old-location: mf\imfmediaengine_getseekable.htm
tech.root: medfound
ms.assetid: FB238892-B172-4E31-B4E5-68C96E135345
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetSeekable, GetSeekable method [Media Foundation], GetSeekable method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetSeekable method, IMFMediaEngine.GetSeekable, IMFMediaEngine::GetSeekable, mf.imfmediaengine_getseekable, mfmediaengine/IMFMediaEngine::GetSeekable
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
 - IMFMediaEngine.GetSeekable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::GetSeekable


## -description


Gets the time ranges to which the Media Engine can currently seek.


## -parameters




### -param ppSeekable

TBD




#### - ppPlayed [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>seekable</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

To find out whether the media source supports seeking, call <a href="https://msdn.microsoft.com/534595D7-007F-450B-A1C7-FA08F3958417">IMFMediaEngineEx::GetResourceCharacteristics</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

