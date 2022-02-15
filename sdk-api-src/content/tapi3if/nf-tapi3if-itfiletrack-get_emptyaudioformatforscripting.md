---
UID: NF:tapi3if.ITFileTrack.get_EmptyAudioFormatForScripting
title: ITFileTrack::get_EmptyAudioFormatForScripting (tapi3if.h)
description: The get_EmptyAudioFormatForScripting method is used to get an ITScriptableAudioFormat interface with all fields set to 0.
helpviewer_keywords: ["ITFileTrack interface [TAPI 2.2]","get_EmptyAudioFormatForScripting method","ITFileTrack.get_EmptyAudioFormatForScripting","ITFileTrack::get_EmptyAudioFormatForScripting","_tapi3_itfiletrack_get_emptyaudioformatforscripting","get_EmptyAudioFormatForScripting","get_EmptyAudioFormatForScripting method [TAPI 2.2]","get_EmptyAudioFormatForScripting method [TAPI 2.2]","ITFileTrack interface","tapi3.itfiletrack_get_emptyaudioformatforscripting","tapi3if/ITFileTrack::get_EmptyAudioFormatForScripting"]
old-location: tapi3\itfiletrack_get_emptyaudioformatforscripting.htm
tech.root: tapi3
ms.assetid: 80644b51-4b04-4299-a486-284e77583feb
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_EmptyAudioFormatForScripting method, ITFileTrack.get_EmptyAudioFormatForScripting, ITFileTrack::get_EmptyAudioFormatForScripting, _tapi3_itfiletrack_get_emptyaudioformatforscripting, get_EmptyAudioFormatForScripting, get_EmptyAudioFormatForScripting method [TAPI 2.2], get_EmptyAudioFormatForScripting method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_emptyaudioformatforscripting, tapi3if/ITFileTrack::get_EmptyAudioFormatForScripting
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
 - ITFileTrack::get_EmptyAudioFormatForScripting
 - tapi3if/ITFileTrack::get_EmptyAudioFormatForScripting
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
 - ITFileTrack.get_EmptyAudioFormatForScripting
---

# ITFileTrack::get_EmptyAudioFormatForScripting


## -description

The 
<b>get_EmptyAudioFormatForScripting</b> method is used to get an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a> interface with all fields set to 0.

## -parameters

### -param ppAudioFormat [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a> interface returned by <b>ITFileTrack::get_EmptyAudioFormatForScripting</b>. The application must call <b>Release</b> on 
<b>ITScriptableAudioFormat</b> to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a>