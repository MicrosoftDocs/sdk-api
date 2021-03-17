---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoVolumeControl
title: ITAutomatedPhoneControl::put_AutoVolumeControl (tapi3if.h)
description: The put_AutoVolumeControl method sets the AutoVolumeControl property for this phone.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoVolumeControl method","ITAutomatedPhoneControl.put_AutoVolumeControl","ITAutomatedPhoneControl::put_AutoVolumeControl","_tapi3_itautomatedphonecontrol_put_autovolumecontrol","put_AutoVolumeControl","put_AutoVolumeControl method [TAPI 2.2]","put_AutoVolumeControl method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autovolumecontrol","tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControl"]
old-location: tapi3\itautomatedphonecontrol_put_autovolumecontrol.htm
tech.root: tapi3
ms.assetid: 3d45ef58-a7d7-41ab-b06a-9d53bf79690a
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoVolumeControl method, ITAutomatedPhoneControl.put_AutoVolumeControl, ITAutomatedPhoneControl::put_AutoVolumeControl, _tapi3_itautomatedphonecontrol_put_autovolumecontrol, put_AutoVolumeControl, put_AutoVolumeControl method [TAPI 2.2], put_AutoVolumeControl method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autovolumecontrol, tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControl
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
 - ITAutomatedPhoneControl::put_AutoVolumeControl
 - tapi3if/ITAutomatedPhoneControl::put_AutoVolumeControl
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
 - ITAutomatedPhoneControl.put_AutoVolumeControl
---

# ITAutomatedPhoneControl::put_AutoVolumeControl


## -description

The 
<b>put_AutoVolumeControl</b> method sets the <b>AutoVolumeControl</b> property for this phone. When this feature is enabled, the phone's wave output volume is automatically adjusted whenever a volume button is pressed. The volume is adjusted by the amount indicated by the <b>AutoVolumeControlStep</b> property.

## -parameters

### -param fEnabled [in]

If VARIANT_TRUE, enables automatic volume control. If VARIANT_FALSE, disables automatic volume control. The default value is VARIANT_TRUE.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoVolumeControl</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoVolumeControl</b> property at any time. The reconfiguration takes effect the next time a volume button is pressed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrol">get_AutoVolumeControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolstep">put_AutoVolumeControlStep</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>