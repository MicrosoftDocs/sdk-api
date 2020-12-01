---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration
title: ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration (tapi3if.h)
description: The get_AutoKeypadTonesMinimumDuration method retrieves the current value of the AutoKeypadTonesMinimumDuration property. The property specifies how long to play keypad tones on PBS_DOWN.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoKeypadTonesMinimumDuration method","ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration","ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration","_tapi3_itautomatedphonecontrol_get_autokeypadtonesminimumduration","get_AutoKeypadTonesMinimumDuration","get_AutoKeypadTonesMinimumDuration method [TAPI 2.2]","get_AutoKeypadTonesMinimumDuration method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autokeypadtonesminimumduration","tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration"]
old-location: tapi3\itautomatedphonecontrol_get_autokeypadtonesminimumduration.htm
tech.root: tapi3
ms.assetid: 9f1ae3f0-ae6a-408a-ac53-e4181ecf2c4b
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoKeypadTonesMinimumDuration method, ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration, ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration, _tapi3_itautomatedphonecontrol_get_autokeypadtonesminimumduration, get_AutoKeypadTonesMinimumDuration, get_AutoKeypadTonesMinimumDuration method [TAPI 2.2], get_AutoKeypadTonesMinimumDuration method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autokeypadtonesminimumduration, tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration
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
 - ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration
 - tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration
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
 - ITAutomatedPhoneControl.get_AutoKeypadTonesMinimumDuration
---

# ITAutomatedPhoneControl::get_AutoKeypadTonesMinimumDuration


## -description

The 
<b>get_AutoKeypadTonesMinimumDuration</b> method retrieves the current value of the <b>AutoKeypadTonesMinimumDuration</b> property. The property specifies how long to play keypad tones on PBS_DOWN.

## -parameters

### -param plDuration [out]

Minimum duration of keypad tones, in milliseconds (ms). The default value is 250 ms. If the minimum duration elapses without a PBS_UP event, the keypad tone continues until the PBS_UP event is received.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoKeypadTonesMinimumDuration</b> property functions only when the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtonesminimumduration">put_AutoKeypadTonesMinimumDuration</a>