---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoVolumeControlRepeatDelay
title: ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay (tapi3if.h)
description: The put_AutoVolumeControlRepeatDelay method sets the AutoVolumeControlRepeatDelay property. The property specifies the delay, in milliseconds (ms), before a volume button starts repeating when it is held down.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoVolumeControlRepeatDelay method","ITAutomatedPhoneControl.put_AutoVolumeControlRepeatDelay","ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay","_tapi3_itautomatedphonecontrol_put_autovolumecontrolrepeatdelay","put_AutoVolumeControlRepeatDelay","put_AutoVolumeControlRepeatDelay method [TAPI 2.2]","put_AutoVolumeControlRepeatDelay method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autovolumecontrolrepeatdelay","tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay"]
old-location: tapi3\itautomatedphonecontrol_put_autovolumecontrolrepeatdelay.htm
tech.root: tapi3
ms.assetid: a00993af-2ff2-4f91-889e-b0d3ae550642
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoVolumeControlRepeatDelay method, ITAutomatedPhoneControl.put_AutoVolumeControlRepeatDelay, ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay, _tapi3_itautomatedphonecontrol_put_autovolumecontrolrepeatdelay, put_AutoVolumeControlRepeatDelay, put_AutoVolumeControlRepeatDelay method [TAPI 2.2], put_AutoVolumeControlRepeatDelay method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autovolumecontrolrepeatdelay, tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay
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
 - ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay
 - tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay
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
 - ITAutomatedPhoneControl.put_AutoVolumeControlRepeatDelay
---

# ITAutomatedPhoneControl::put_AutoVolumeControlRepeatDelay


## -description

The 
<b>put_AutoVolumeControlRepeatDelay</b> method sets the <b>AutoVolumeControlRepeatDelay</b> property. The property specifies the delay, in milliseconds (ms), before a volume button starts repeating when it is held down.

## -parameters

### -param lDelay [in]

Delay, in milliseconds (ms), before the volume button starts repeating. The default value is 500 ms.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrolrepeatdelay">get_AutoVolumeControlRepeatDelay</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>