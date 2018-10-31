---
UID: NF:mfmediaengine.IMFMediaEngineEx.FrameStep
title: IMFMediaEngineEx::FrameStep
author: windows-sdk-content
description: Steps forward or backward one frame.
old-location: mf\imfmediaengineex_framestep.htm
tech.root: medfound
ms.assetid: 090B5B6F-E4D1-43D7-AD09-BA3008B48104
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FrameStep, FrameStep method [Media Foundation], FrameStep method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],FrameStep method, IMFMediaEngineEx.FrameStep, IMFMediaEngineEx::FrameStep, mf.imfmediaengineex_framestep, mfmediaengine/IMFMediaEngineEx::FrameStep
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
 - IMFMediaEngineEx.FrameStep
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::FrameStep


## -description


Steps forward or backward one frame.


## -parameters




### -param Forward [in]

Specify <b>TRUE</b> to step forward or <b>FALSE</b> to step backward.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The frame-step direction is independent of the current playback direction.

This method completes asynchronously. When the operation completes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_FRAMESTEPCOMPLETED</b> event and enters the paused state.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

