---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoKeypadTones
title: ITAutomatedPhoneControl::put_AutoKeypadTones (tapi3if.h)
description: The put_AutoKeypadTones method sets the AutoKeypadTones property for this phone. When this feature is enabled, a digit tone is automatically played whenever a keypad button is pressed.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoKeypadTones method","ITAutomatedPhoneControl.put_AutoKeypadTones","ITAutomatedPhoneControl::put_AutoKeypadTones","_tapi3_itautomatedphonecontrol_put_autokeypadtones","put_AutoKeypadTones","put_AutoKeypadTones method [TAPI 2.2]","put_AutoKeypadTones method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autokeypadtones","tapi3if/ITAutomatedPhoneControl::put_AutoKeypadTones"]
old-location: tapi3\itautomatedphonecontrol_put_autokeypadtones.htm
tech.root: tapi3
ms.assetid: 5a57c0ef-440a-4939-8d15-edb0c59dc1a4
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoKeypadTones method, ITAutomatedPhoneControl.put_AutoKeypadTones, ITAutomatedPhoneControl::put_AutoKeypadTones, _tapi3_itautomatedphonecontrol_put_autokeypadtones, put_AutoKeypadTones, put_AutoKeypadTones method [TAPI 2.2], put_AutoKeypadTones method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autokeypadtones, tapi3if/ITAutomatedPhoneControl::put_AutoKeypadTones
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
 - ITAutomatedPhoneControl::put_AutoKeypadTones
 - tapi3if/ITAutomatedPhoneControl::put_AutoKeypadTones
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
 - ITAutomatedPhoneControl.put_AutoKeypadTones
---

# ITAutomatedPhoneControl::put_AutoKeypadTones


## -description

The 
<b>put_AutoKeypadTones</b> method sets the <b>AutoKeypadTones</b> property for this phone. When this feature is enabled, a digit tone is automatically played whenever a keypad button is pressed.

## -parameters

### -param fEnabled [in]

If VARIANT_TRUE, automatic phone keypad tone generation is enabled. If VARIANT_FALSE, keypad tone generation is disabled. The default value is VARIANT_TRUE.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

If the phone device reports a button press as PBS_DOWN, then the tone is played until the phone device reports a PBS_UP event or until the minimum duration has expired, whichever is longer. (The minimum duration is determined by the <b>AutoKeypadTonesMinimumDuration</b> property.)

Keypad tone generation will occur only when the phone is offhook. If another tone, such as ringback, is currently playing, the keypad tone will interrupt that tone and automatically restore it after the keypad tone has finished.

The <b>AutoKeypadTones</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoKeypadTones</b> property at any time. The reconfiguration takes effect the next time the phone keypad button is pressed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autokeypadtones">get_AutoKeypadTones</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtonesminimumduration">put_AutoKeypadTonesMinimumDuration</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>