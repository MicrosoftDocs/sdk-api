---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay
title: ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay (tapi3if.h)
description: The get_AutoVolumeControlRepeatDelay method retrieves the current value of the AutoVolumeControlRepeatDelay property. The property specifies the delay, in milliseconds (ms), before a volume button starts repeating when it is held down.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoVolumeControlRepeatDelay method","ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay","ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay","_tapi3_itautomatedphonecontrol_get_autovolumecontrolrepeatdelay","get_AutoVolumeControlRepeatDelay","get_AutoVolumeControlRepeatDelay method [TAPI 2.2]","get_AutoVolumeControlRepeatDelay method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autovolumecontrolrepeatdelay","tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay"]
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrolrepeatdelay.htm
tech.root: tapi3
ms.assetid: a26fd436-b792-4415-bc47-eca2b1114002
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControlRepeatDelay method, ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay, ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay, _tapi3_itautomatedphonecontrol_get_autovolumecontrolrepeatdelay, get_AutoVolumeControlRepeatDelay, get_AutoVolumeControlRepeatDelay method [TAPI 2.2], get_AutoVolumeControlRepeatDelay method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrolrepeatdelay, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay
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
 - ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay
 - tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay
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
 - ITAutomatedPhoneControl.get_AutoVolumeControlRepeatDelay
---

# ITAutomatedPhoneControl::get_AutoVolumeControlRepeatDelay


## -description

The 
<b>get_AutoVolumeControlRepeatDelay</b> method retrieves the current value of the <b>AutoVolumeControlRepeatDelay</b> property. The property specifies the delay, in milliseconds (ms), before a volume button starts repeating when it is held down.

## -parameters

### -param plDelay [out]

Delay, in milliseconds, of the volume repeat delay. The default value is 500 ms.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolrepeatdelay">put_AutoVolumeControlRepeatDelay</a>