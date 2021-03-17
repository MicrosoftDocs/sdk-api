---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoVolumeControl
title: ITAutomatedPhoneControl::get_AutoVolumeControl (tapi3if.h)
description: The get_AutoVolumeControl method retrieves the current value of the AutoVolumeControl property.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoVolumeControl method","ITAutomatedPhoneControl.get_AutoVolumeControl","ITAutomatedPhoneControl::get_AutoVolumeControl","_tapi3_itautomatedphonecontrol_get_autovolumecontrol","get_AutoVolumeControl","get_AutoVolumeControl method [TAPI 2.2]","get_AutoVolumeControl method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autovolumecontrol","tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControl"]
old-location: tapi3\itautomatedphonecontrol_get_autovolumecontrol.htm
tech.root: tapi3
ms.assetid: 7dae6d41-59d8-40ab-901f-91d97b59ac83
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoVolumeControl method, ITAutomatedPhoneControl.get_AutoVolumeControl, ITAutomatedPhoneControl::get_AutoVolumeControl, _tapi3_itautomatedphonecontrol_get_autovolumecontrol, get_AutoVolumeControl, get_AutoVolumeControl method [TAPI 2.2], get_AutoVolumeControl method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autovolumecontrol, tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControl
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
 - ITAutomatedPhoneControl::get_AutoVolumeControl
 - tapi3if/ITAutomatedPhoneControl::get_AutoVolumeControl
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
 - ITAutomatedPhoneControl.get_AutoVolumeControl
---

# ITAutomatedPhoneControl::get_AutoVolumeControl


## -description

The 
<b>get_AutoVolumeControl</b> method retrieves the current value of the <b>AutoVolumeControl</b> property. When this feature is enabled, the phone's wave output volume is automatically adjusted whenever a volume button is pressed. The volume is adjusted by the amount indicated by the <b>AutoVolumeControlStep</b> property.

## -parameters

### -param fEnabled [out]

VARIANT_TRUE indicates that automatic volume control is enabled. VARIANT_FALSE indicates that automatic volume control is disabled.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

You can set the <b>AutoVolumeControl</b> property at any time. The reconfiguration takes effect the next time a volume button is pressed.

The <b>AutoVolumeControl</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrol">put_AutoVolumeControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolstep">put_AutoVolumeControlStep</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>