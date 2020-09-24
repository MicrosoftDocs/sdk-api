---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_Ringer
title: ITAutomatedPhoneControl::get_Ringer (tapi3if.h)
description: The get_Ringer method returns a Boolean value indicating whether the phone is currently performing an incoming ring that was initiated by the StartRinger method on this interface.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_Ringer method","ITAutomatedPhoneControl.get_Ringer","ITAutomatedPhoneControl::get_Ringer","_tapi3_itautomatedphonecontrol_get_ringer","get_Ringer","get_Ringer method [TAPI 2.2]","get_Ringer method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_ringer","tapi3if/ITAutomatedPhoneControl::get_Ringer"]
old-location: tapi3\itautomatedphonecontrol_get_ringer.htm
tech.root: tapi3
ms.assetid: cc4daec0-7f55-4c76-b8a0-19307c7046dc
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_Ringer method, ITAutomatedPhoneControl.get_Ringer, ITAutomatedPhoneControl::get_Ringer, _tapi3_itautomatedphonecontrol_get_ringer, get_Ringer, get_Ringer method [TAPI 2.2], get_Ringer method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_ringer, tapi3if/ITAutomatedPhoneControl::get_Ringer
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
 - ITAutomatedPhoneControl::get_Ringer
 - tapi3if/ITAutomatedPhoneControl::get_Ringer
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
 - ITAutomatedPhoneControl.get_Ringer
---

# ITAutomatedPhoneControl::get_Ringer


## -description

The 
<b>get_Ringer</b> method returns a Boolean value indicating whether the phone is currently performing an incoming ring that was initiated by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-startringer">StartRinger</a> method on this interface.

## -parameters

### -param pfRinging [out]

If VARIANT_TRUE, the phone is currently ringing.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-startringer">StartRinger</a>