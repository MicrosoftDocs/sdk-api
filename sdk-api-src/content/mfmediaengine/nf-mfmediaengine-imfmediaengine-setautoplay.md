---
UID: NF:mfmediaengine.IMFMediaEngine.SetAutoPlay
title: IMFMediaEngine::SetAutoPlay
author: windows-sdk-content
description: Specifies whether the Media Engine automatically begins playback.
old-location: mf\imfmediaengine_setautoplay.htm
tech.root: medfound
ms.assetid: 867FE1D2-39AE-4A44-99DD-98A8ABD234A2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetAutoPlay method, IMFMediaEngine.SetAutoPlay, IMFMediaEngine::SetAutoPlay, SetAutoPlay, SetAutoPlay method [Media Foundation], SetAutoPlay method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setautoplay, mfmediaengine/IMFMediaEngine::SetAutoPlay
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
 - IMFMediaEngine.SetAutoPlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::SetAutoPlay


## -description


Specifies whether the Media Engine automatically begins playback.


## -parameters




### -param AutoPlay [in]

If <b>TRUE</b>, the Media Engine automatically begins playback after it loads a media source. Otherwise, playback does not begin until the application calls <a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">IMFMediaEngine::Play</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to setting the <b>autoplay</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

