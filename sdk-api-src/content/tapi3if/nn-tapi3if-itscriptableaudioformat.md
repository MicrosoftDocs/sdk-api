---
UID: NN:tapi3if.ITScriptableAudioFormat
title: ITScriptableAudioFormat (tapi3if.h)
description: The ITScriptableAudioFormat interface is used by scriptable clients to get the audio format from, or set the audio format for, the track. The interface provides properties for each member from the WAVEFORMATEX structure.
helpviewer_keywords: ["ITScriptableAudioFormat","ITScriptableAudioFormat interface [TAPI 2.2]","ITScriptableAudioFormat interface [TAPI 2.2]","described","_tapi3_itscriptableaudioformat","tapi3.itscriptableaudioformat","tapi3if/ITScriptableAudioFormat"]
old-location: tapi3\itscriptableaudioformat.htm
tech.root: tapi3
ms.assetid: 6b5d069a-044f-4bd4-b661-6100a2607107
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat, ITScriptableAudioFormat interface [TAPI 2.2], ITScriptableAudioFormat interface [TAPI 2.2],described, _tapi3_itscriptableaudioformat, tapi3.itscriptableaudioformat, tapi3if/ITScriptableAudioFormat
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
 - ITScriptableAudioFormat
 - tapi3if/ITScriptableAudioFormat
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
 - ITScriptableAudioFormat
---

# ITScriptableAudioFormat interface


## -description

The 
<b>ITScriptableAudioFormat</b> interface is used by scriptable clients to get the audio format from, or set the audio format for, the track. The interface provides properties for each member from the 
<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_audioformatforscripting">ITFileTrack::get_AudioFormatForScripting</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_emptyaudioformatforscripting">ITFileTrack::get_EmptyAudioFormatForScripting</a> methods create the 
<b>ITScriptableAudioFormat</b> interface.

## -inheritance

The <b>ITScriptableAudioFormat</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITScriptableAudioFormat</b> also has these types of members:

