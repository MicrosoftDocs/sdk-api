---
UID: NF:xapo.IXAPO.Reset
title: IXAPO::Reset
author: windows-sdk-content
description: Resets variables dependent on frame history.
old-location: xaudio2\ixapo_interface_reset.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.Reset
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],Reset method, IXAPO.Reset, IXAPO::Reset, Reset, Reset method [XAudio2 Audio Mixing APIs], Reset method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::Reset, xaudio2.ixapo_interface_reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
req.include-header: 
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
 - IXAPO.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::Reset


## -description


Resets variables dependent on frame history.


## -parameters






## -returns



This method does not return a value.




## -remarks



Constant and locked parameters such as the input and output formats remain unchanged. Variables set by <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> remain unchanged.



For example, an effect with delay should zero out its delay line during this method, but should not reallocate anything as the XAPO remains locked with a constant input and output configuration.



XAudio2 only calls this method if the XAPO is locked.



This method is called from the realtime thread and should not block.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

