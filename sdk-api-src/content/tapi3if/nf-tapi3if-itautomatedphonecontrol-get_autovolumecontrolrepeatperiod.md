---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControlRepeatPeriod
title: ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod (tapi3if.h)
description: The get_AutoVolumeControlRepeatPeriod method retrieves the current value of the AutoVolumeControlRepeatPeriod property. The property controls the period, in milliseconds (ms), of button repeats when a volume button is held down.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoVolumeControlRepeatPeriod method","ITAutomatedPhoneControl.get_AutoVolumeControlRepeatPeriod","ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod","_tapi3_itautomatedphonecontrol_get_autovolumecontrolrepeatperiod","get_AutoVolumeControlRepeatPeriod","get_AutoVolumeControlRepeatPeriod method [TAPI 2.2]","get_AutoVolumeControlRepeatPeriod method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autovolumecontrolrepeatperiod","tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod"]
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrolrepeatperiod.htm
tech.root: tapi3
ms.assetid: 6ab52127-62e2-4e80-980a-8b29b51fa91f
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControlRepeatPeriod method, ITAutomatedPhoneControl.get_AutoVolumeControlRepeatPeriod, ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod, _tapi3_itautomatedphonecontrol_get_autovolumecontrolrepeatperiod, get_AutoVolumeControlRepeatPeriod, get_AutoVolumeControlRepeatPeriod method [TAPI 2.2], get_AutoVolumeControlRepeatPeriod method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrolrepeatperiod, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod
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
 - ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod
 - tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod
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
 - ITAutomatedPhoneControl.get_AutoVolumeControlRepeatPeriod
---

# ITAutomatedPhoneControl::get_AutoVolumeControlRepeatPeriod


## -description

The 
<b>get_AutoVolumeControlRepeatPeriod</b> method retrieves the current value of the <b>AutoVolumeControlRepeatPeriod</b> property. The property controls the period, in milliseconds (ms), of button repeats when a volume button is held down.

## -parameters

### -param plPeriod [out]

Period, in milliseconds (ms), of button repeats when a volume button is held down.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoVolumeControlRepeatDelay</b> property is valid only if the value of the <b>AutoKeypadTones</b> property is VARIANT_TRUE.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolrepeatperiod">put_AutoVolumeControlRepeatPeriod</a>