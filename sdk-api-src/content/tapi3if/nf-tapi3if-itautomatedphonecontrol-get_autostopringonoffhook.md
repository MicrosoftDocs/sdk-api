---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoStopRingOnOffHook
title: ITAutomatedPhoneControl::get_AutoStopRingOnOffHook (tapi3if.h)
description: The get_AutoStopRingOnOffHook method retrieves the current value of the AutoStopRingOnOffHook property.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoStopRingOnOffHook method","ITAutomatedPhoneControl.get_AutoStopRingOnOffHook","ITAutomatedPhoneControl::get_AutoStopRingOnOffHook","_tapi3_itautomatedphonecontrol_get_autostopringonoffhook","get_AutoStopRingOnOffHook","get_AutoStopRingOnOffHook method [TAPI 2.2]","get_AutoStopRingOnOffHook method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autostopringonoffhook","tapi3if/ITAutomatedPhoneControl::get_AutoStopRingOnOffHook"]
old-location: tapi3\itautomatedphonecontrol_get_autostopringonoffhook.htm
tech.root: tapi3
ms.assetid: 357266e7-b103-43c1-a6af-b00347c90f51
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoStopRingOnOffHook method, ITAutomatedPhoneControl.get_AutoStopRingOnOffHook, ITAutomatedPhoneControl::get_AutoStopRingOnOffHook, _tapi3_itautomatedphonecontrol_get_autostopringonoffhook, get_AutoStopRingOnOffHook, get_AutoStopRingOnOffHook method [TAPI 2.2], get_AutoStopRingOnOffHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autostopringonoffhook, tapi3if/ITAutomatedPhoneControl::get_AutoStopRingOnOffHook
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
 - ITAutomatedPhoneControl::get_AutoStopRingOnOffHook
 - tapi3if/ITAutomatedPhoneControl::get_AutoStopRingOnOffHook
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
 - ITAutomatedPhoneControl.get_AutoStopRingOnOffHook
---

# ITAutomatedPhoneControl::get_AutoStopRingOnOffHook


## -description

The 
<b>get_AutoStopRingOnOffHook</b> method retrieves the current value of the <b>AutoStopRingOnOffHook</b> property. When this feature is enabled, the phone going offhook results in the termination of any incoming ring produced on the phone (via a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stopringer">ITAutomatedPhoneControl::StopRinger</a>).

## -parameters

### -param pfEnabled [out]

If VARIANT_TRUE, automatic incoming ring termination when the phone goes offhook is enabled. If VARIANT_FALSE, automatic incoming ring termination when the phone goes offhook is disabled.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoStopRingOnOffHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopRingOnOffHook</b> property at any time. The reconfiguration takes effect the next time the phone goes offhook.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stopringer">ITAutomatedPhoneControl::StopRinger</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autostopringonoffhook">put_AutoStopRingOnOffHook</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>