---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetCurrentTimeEx
title: IMFMediaEngineEx::SetCurrentTimeEx (mfmediaengine.h)
author: windows-sdk-content
description: Seeks to a new playback position using the specified MF_MEDIA_ENGINE_SEEK_MODE.
old-location: mf\imfmediaengineex_setcurrenttimeex.htm
tech.root: medfound
ms.assetid: ee594f0c-af49-44c2-8c68-16120f76c5e1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetCurrentTimeEx method, IMFMediaEngineEx.SetCurrentTimeEx, IMFMediaEngineEx::SetCurrentTimeEx, SetCurrentTimeEx, SetCurrentTimeEx method [Media Foundation], SetCurrentTimeEx method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setcurrenttimeex, mfmediaengine/IMFMediaEngineEx::SetCurrentTimeEx
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
 - IMFMediaEngineEx.SetCurrentTimeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::SetCurrentTimeEx


## -description


Seeks to a new playback position using the  specified <a href="https://msdn.microsoft.com/58356FC2-5F1E-463F-98D5-E63AFCC05A02">MF_MEDIA_ENGINE_SEEK_MODE</a>.


## -parameters




### -param seekTime [in]

The new playback position, in seconds.


### -param seekMode [in]

Specifies if the seek is a normal seek or an approximate seek.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

