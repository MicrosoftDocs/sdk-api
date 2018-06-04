---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITStaticAudioTerminal::get_WaveId


## -description


The 
<b>get_WaveId</b> method returns the wave ID for the audio device used to implement this terminal.


## -parameters




### -param plWaveId [out]

Pointer to a variable where, on success, the method will store the wave ID for this terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



All MSPs must implement the 
<b>get_WaveId</b> method on their audio terminals for TAPI's association of phone devices and audio terminals to work for calls on that MSP's addresses. See 
<a href="https://msdn.microsoft.com/154c07b6-c693-469d-819a-f6d2d2afd744">ITStaticAudioTerminal</a> for what to do for audio terminals that are not accessible via standard Windows audio APIs.

All other terminals must return the correct wave ID, even if the internal implementation of the terminal does not use wave. In such cases, a mapping should be possible between the identifier used in the nonwave APIs and the wave ID. The MSP must perform this mapping.




## -see-also




<a href="https://msdn.microsoft.com/154c07b6-c693-469d-819a-f6d2d2afd744">ITStaticAudioTerminal</a>
 

 

