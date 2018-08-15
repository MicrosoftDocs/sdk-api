---
UID: NF:mfmediaengine.IMFMediaEngine.SetVolume
title: IMFMediaEngine::SetVolume
author: windows-sdk-content
description: Sets the audio volume level.
old-location: mf\imfmediaengine_setvolume.htm
old-project: medfound
ms.assetid: 010EE05C-3F81-404E-8AFB-7C57CA55A8AE
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetVolume method, IMFMediaEngine.SetVolume, IMFMediaEngine::SetVolume, SetVolume, SetVolume method [Media Foundation], SetVolume method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setvolume, mfmediaengine/IMFMediaEngine::SetVolume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
 - IMFMediaEngine.SetVolume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::SetVolume


## -description


Sets the audio volume level.


## -parameters




### -param Volume [in]

The volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the audio balance changes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_VOLUMECHANGE</b> event. See <a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEventNotify::EventNotify</a>.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

