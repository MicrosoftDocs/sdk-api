---
UID: NF:tapi3if.ITStaticAudioTerminal.get_WaveId
title: ITStaticAudioTerminal::get_WaveId (tapi3if.h)
description: The get_WaveId method returns the wave ID for the audio device used to implement this terminal.
helpviewer_keywords: ["ITStaticAudioTerminal interface [TAPI 2.2]","get_WaveId method","ITStaticAudioTerminal.get_WaveId","ITStaticAudioTerminal::get_WaveId","_tapi3_itstaticaudioterminal_get_waveid","get_WaveId","get_WaveId method [TAPI 2.2]","get_WaveId method [TAPI 2.2]","ITStaticAudioTerminal interface","tapi3.itstaticaudioterminal_get_waveid","tapi3if/ITStaticAudioTerminal::get_WaveId"]
old-location: tapi3\itstaticaudioterminal_get_waveid.htm
tech.root: tapi3
ms.assetid: dbbfbfe0-843b-4baf-b4f5-51a3037c5fd9
ms.date: 12/05/2018
ms.keywords: ITStaticAudioTerminal interface [TAPI 2.2],get_WaveId method, ITStaticAudioTerminal.get_WaveId, ITStaticAudioTerminal::get_WaveId, _tapi3_itstaticaudioterminal_get_waveid, get_WaveId, get_WaveId method [TAPI 2.2], get_WaveId method [TAPI 2.2],ITStaticAudioTerminal interface, tapi3.itstaticaudioterminal_get_waveid, tapi3if/ITStaticAudioTerminal::get_WaveId
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITStaticAudioTerminal::get_WaveId
 - tapi3if/ITStaticAudioTerminal::get_WaveId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITStaticAudioTerminal.get_WaveId
---

# ITStaticAudioTerminal::get_WaveId


## -description

The 
<b>get_WaveId</b> method returns the wave ID for the audio device used to implement this terminal.

## -parameters

### -param plWaveId [out]

Pointer to a variable where, on success, the method will store the wave ID for this terminal.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

All MSPs must implement the 
<b>get_WaveId</b> method on their audio terminals for TAPI's association of phone devices and audio terminals to work for calls on that MSP's addresses. See 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal">ITStaticAudioTerminal</a> for what to do for audio terminals that are not accessible via standard Windows audio APIs.

All other terminals must return the correct wave ID, even if the internal implementation of the terminal does not use wave. In such cases, a mapping should be possible between the identifier used in the nonwave APIs and the wave ID. The MSP must perform this mapping.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal">ITStaticAudioTerminal</a>