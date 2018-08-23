---
UID: NF:xapo.IXAPO.CalcOutputFrames
title: IXAPO::CalcOutputFrames
author: windows-sdk-content
description: Returns the number of output frames that will be generated from a given number of input frames.
old-location: xaudio2\ixapo_interface_calcoutputframes.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.CalcOutputFrames(UINT32)
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CalcOutputFrames, CalcOutputFrames method [XAudio2 Audio Mixing APIs], CalcOutputFrames method [XAudio2 Audio Mixing APIs],IXAPO interface, IXAPO interface [XAudio2 Audio Mixing APIs],CalcOutputFrames method, IXAPO.CalcOutputFrames, IXAPO::CalcOutputFrames, xapo/IXAPO::CalcOutputFrames, xaudio2.ixapo_interface_calcoutputframes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: XAPO_BUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.CalcOutputFrames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::CalcOutputFrames


## -description


Returns the number of output frames that will be generated from a given number of input frames.


## -parameters




### -param InputFrameCount

The number of input frames.



## -returns



Returns the number of output frames that will be produced.






## -remarks



XAudio2 calls this method to determine how large of an output buffer an XAPO will require for a certain number of input frames. <b>CalcOutputFrames</b> is only called by XAudio2 if the XAPO is locked.



This function should not block, because it may be called from the realtime audio processing thread.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

