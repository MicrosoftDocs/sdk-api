---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_Tone
title: ITAutomatedPhoneControl::get_Tone (tapi3if.h)
description: The get_Tone method returns a PHONE_TONE enum value indicating the type of tone, if any, that the phone is currently playing.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_Tone method","ITAutomatedPhoneControl.get_Tone","ITAutomatedPhoneControl::get_Tone","_tapi3_itautomatedphonecontrol_get_tone","get_Tone","get_Tone method [TAPI 2.2]","get_Tone method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_tone","tapi3if/ITAutomatedPhoneControl::get_Tone"]
old-location: tapi3\itautomatedphonecontrol_get_tone.htm
tech.root: tapi3
ms.assetid: 62e7ae4d-7839-4568-b8b2-7a377601ea7c
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_Tone method, ITAutomatedPhoneControl.get_Tone, ITAutomatedPhoneControl::get_Tone, _tapi3_itautomatedphonecontrol_get_tone, get_Tone, get_Tone method [TAPI 2.2], get_Tone method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_tone, tapi3if/ITAutomatedPhoneControl::get_Tone
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
 - ITAutomatedPhoneControl::get_Tone
 - tapi3if/ITAutomatedPhoneControl::get_Tone
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
 - ITAutomatedPhoneControl.get_Tone
---

# ITAutomatedPhoneControl::get_Tone


## -description

The 
<b>get_Tone</b> method returns a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_tone">PHONE_TONE</a> enum value indicating the type of tone, if any, that the phone is currently playing. If no tone is currently being played, the 
<b>PHONE_TONE</b> value returned is PT_SILENCE. This method has knowledge only of tones initiated by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-starttone">StartTone</a> method on this interface.

## -parameters

### -param pTone [out]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_tone">PHONE_TONE</a> descriptor of tone being played.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-starttone">StartTone</a>