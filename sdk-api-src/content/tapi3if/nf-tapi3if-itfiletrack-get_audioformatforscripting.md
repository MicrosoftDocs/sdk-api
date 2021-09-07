---
UID: NF:tapi3if.ITFileTrack.get_AudioFormatForScripting
title: ITFileTrack::get_AudioFormatForScripting (tapi3if.h)
description: The get_AudioFormatForScripting method gets the audio scripting format.
helpviewer_keywords: ["ITFileTrack interface [TAPI 2.2]","get_AudioFormatForScripting method","ITFileTrack.get_AudioFormatForScripting","ITFileTrack::get_AudioFormatForScripting","_tapi3_itfiletrack_get_audioformatforscripting","get_AudioFormatForScripting","get_AudioFormatForScripting method [TAPI 2.2]","get_AudioFormatForScripting method [TAPI 2.2]","ITFileTrack interface","tapi3.itfiletrack_get_audioformatforscripting","tapi3if/ITFileTrack::get_AudioFormatForScripting"]
old-location: tapi3\itfiletrack_get_audioformatforscripting.htm
tech.root: tapi3
ms.assetid: 3677b85c-15a4-4960-88ad-18855349fedd
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_AudioFormatForScripting method, ITFileTrack.get_AudioFormatForScripting, ITFileTrack::get_AudioFormatForScripting, _tapi3_itfiletrack_get_audioformatforscripting, get_AudioFormatForScripting, get_AudioFormatForScripting method [TAPI 2.2], get_AudioFormatForScripting method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_audioformatforscripting, tapi3if/ITFileTrack::get_AudioFormatForScripting
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
 - ITFileTrack::get_AudioFormatForScripting
 - tapi3if/ITFileTrack::get_AudioFormatForScripting
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
 - ITFileTrack.get_AudioFormatForScripting
---

# ITFileTrack::get_AudioFormatForScripting


## -description

The 
<b>get_AudioFormatForScripting</b> method gets the audio scripting format.

## -parameters

### -param ppAudioFormat [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a> interface returned by <b>ITFileTrack::get_AudioFormatForScripting</b>. The application must call <b>Release</b> on 
<b>ITScriptableAudioFormat</b> to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a>