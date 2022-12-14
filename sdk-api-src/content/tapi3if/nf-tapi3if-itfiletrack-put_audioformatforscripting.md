---
UID: NF:tapi3if.ITFileTrack.put_AudioFormatForScripting
title: ITFileTrack::put_AudioFormatForScripting (tapi3if.h)
description: The put_AudioFormatForScripting method sets the audio scripting format.
helpviewer_keywords: ["ITFileTrack interface [TAPI 2.2]","put_AudioFormatForScripting method","ITFileTrack.put_AudioFormatForScripting","ITFileTrack::put_AudioFormatForScripting","_tapi3_itfiletrack_put_audioformatforscripting","put_AudioFormatForScripting","put_AudioFormatForScripting method [TAPI 2.2]","put_AudioFormatForScripting method [TAPI 2.2]","ITFileTrack interface","tapi3.itfiletrack_put_audioformatforscripting","tapi3if/ITFileTrack::put_AudioFormatForScripting"]
old-location: tapi3\itfiletrack_put_audioformatforscripting.htm
tech.root: tapi3
ms.assetid: a5ec8ede-8801-418d-9264-415b78abb336
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],put_AudioFormatForScripting method, ITFileTrack.put_AudioFormatForScripting, ITFileTrack::put_AudioFormatForScripting, _tapi3_itfiletrack_put_audioformatforscripting, put_AudioFormatForScripting, put_AudioFormatForScripting method [TAPI 2.2], put_AudioFormatForScripting method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_put_audioformatforscripting, tapi3if/ITFileTrack::put_AudioFormatForScripting
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
 - ITFileTrack::put_AudioFormatForScripting
 - tapi3if/ITFileTrack::put_AudioFormatForScripting
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
 - ITFileTrack.put_AudioFormatForScripting
---

# ITFileTrack::put_AudioFormatForScripting


## -description

The 
<b>put_AudioFormatForScripting</b> method sets the audio scripting format.

## -parameters

### -param pAudioFormat [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a>