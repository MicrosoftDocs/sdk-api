---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoKeypadTones
title: ITAutomatedPhoneControl::get_AutoKeypadTones (tapi3if.h)
description: The get_AutoKeypadTones method gets the AutoKeypadTones property for this phone. When this feature is enabled, a digit tone is automatically played whenever a keypad button is pressed.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoKeypadTones method","ITAutomatedPhoneControl.get_AutoKeypadTones","ITAutomatedPhoneControl::get_AutoKeypadTones","_tapi3_itautomatedphonecontrol_get_autokeypadtones","get_AutoKeypadTones","get_AutoKeypadTones method [TAPI 2.2]","get_AutoKeypadTones method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autokeypadtones","tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTones"]
old-location: tapi3\itautomatedphonecontrol_get_autokeypadtones.htm
tech.root: tapi3
ms.assetid: fd6c2b1c-53c5-40f9-bb5e-51c48d5bc944
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoKeypadTones method, ITAutomatedPhoneControl.get_AutoKeypadTones, ITAutomatedPhoneControl::get_AutoKeypadTones, _tapi3_itautomatedphonecontrol_get_autokeypadtones, get_AutoKeypadTones, get_AutoKeypadTones method [TAPI 2.2], get_AutoKeypadTones method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autokeypadtones, tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTones
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
 - ITAutomatedPhoneControl::get_AutoKeypadTones
 - tapi3if/ITAutomatedPhoneControl::get_AutoKeypadTones
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
 - ITAutomatedPhoneControl.get_AutoKeypadTones
---

# ITAutomatedPhoneControl::get_AutoKeypadTones


## -description

The 
<b>get_AutoKeypadTones</b> method gets the <b>AutoKeypadTones</b> property for this phone. When this feature is enabled, a digit tone is automatically played whenever a keypad button is pressed.

## -parameters

### -param pfEnabled [out]

VARIANT_TRUE if automatic phone keypad feedback tone generation is enabled for this phone. VARIANT_FALSE if automatic phone keypad feedback tone generation is disabled for this phone.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

If the phone device reports a button press as PBS_DOWN, then the tone is played until the phone device reports a PBS_UP event or until the minimum duration has expired, whichever is longer. (The minimum duration is determined by the <b>AutoKeypadTonesMinimumDuration</b> property.)

Keypad tone generation will occur only when the phone is offhook. If another tone, such as ringback, is currently playing, the keypad tone will interrupt that tone and automatically restore it after the keypad tone has finished.

The <b>AutoKeypadTones</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoKeypadTones</b> property at any time. The reconfiguration takes effect the next time the phone keypad button is pressed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtonesminimumduration">put_AutoKeypadTonesMinimumDuration</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>