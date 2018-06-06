---
UID: NF:xapo.IXAPO.UnlockForProcess
title: IXAPO::UnlockForProcess
author: windows-sdk-content
description: Deallocates variables that were allocated with the LockForProcess method.
old-location: xaudio2\ixapo_interface_unlockforprocess.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.UnlockForProcess
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],UnlockForProcess method, IXAPO.UnlockForProcess, IXAPO::UnlockForProcess, UnlockForProcess, UnlockForProcess method [XAudio2 Audio Mixing APIs], UnlockForProcess method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::UnlockForProcess, xaudio2.ixapo_interface_unlockforprocess
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
 - IXAPO.UnlockForProcess
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::UnlockForProcess


## -description


Deallocates variables that were allocated with the <a href="https://msdn.microsoft.com/2143A204-342F-4A78-A6D7-D319360A3948">LockForProcess</a> method.


## -parameters






## -returns



This method does not return a value.




## -remarks



Unlocking an XAPO instance allows it to be reused with different input and output formats.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

