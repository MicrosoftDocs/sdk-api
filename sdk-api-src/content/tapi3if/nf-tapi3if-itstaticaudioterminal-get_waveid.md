---
UID: NF:tapi3if.ITStaticAudioTerminal.get_WaveId
title: ITStaticAudioTerminal::get_WaveId
author: windows-sdk-content
description: The get_WaveId method returns the wave ID for the audio device used to implement this terminal.
old-location: tapi3\itstaticaudioterminal_get_waveid.htm
old-project: tapi
ms.assetid: dbbfbfe0-843b-4baf-b4f5-51a3037c5fd9
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITStaticAudioTerminal interface [TAPI 2.2],get_WaveId method, ITStaticAudioTerminal.get_WaveId, ITStaticAudioTerminal::get_WaveId, _tapi3_itstaticaudioterminal_get_waveid, get_WaveId, get_WaveId method [TAPI 2.2], get_WaveId method [TAPI 2.2],ITStaticAudioTerminal interface, tapi3.itstaticaudioterminal_get_waveid, tapi3if/ITStaticAudioTerminal::get_WaveId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITStaticAudioTerminal.get_WaveId
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

