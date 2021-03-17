---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoStopRingOnOffHook
title: ITAutomatedPhoneControl::put_AutoStopRingOnOffHook (tapi3if.h)
description: The put_AutoStopRingOnOffHook method sets the AutoStopRingOnOffHook property. When this feature is enabled, the phone going offhook results in the termination of any incoming ring produced on the phone (via a call to ITAutomatedPhoneControl::StopRinger).
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoStopRingOnOffHook method","ITAutomatedPhoneControl.put_AutoStopRingOnOffHook","ITAutomatedPhoneControl::put_AutoStopRingOnOffHook","_tapi3_itautomatedphonecontrol_put_autostopringonoffhook","put_AutoStopRingOnOffHook","put_AutoStopRingOnOffHook method [TAPI 2.2]","put_AutoStopRingOnOffHook method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autostopringonoffhook","tapi3if/ITAutomatedPhoneControl::put_AutoStopRingOnOffHook"]
old-location: tapi3\itautomatedphonecontrol_put_autostopringonoffhook.htm
tech.root: tapi3
ms.assetid: 114e17e2-63e7-47f9-8ae7-1c7e452376f6
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoStopRingOnOffHook method, ITAutomatedPhoneControl.put_AutoStopRingOnOffHook, ITAutomatedPhoneControl::put_AutoStopRingOnOffHook, _tapi3_itautomatedphonecontrol_put_autostopringonoffhook, put_AutoStopRingOnOffHook, put_AutoStopRingOnOffHook method [TAPI 2.2], put_AutoStopRingOnOffHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autostopringonoffhook, tapi3if/ITAutomatedPhoneControl::put_AutoStopRingOnOffHook
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
 - ITAutomatedPhoneControl::put_AutoStopRingOnOffHook
 - tapi3if/ITAutomatedPhoneControl::put_AutoStopRingOnOffHook
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
 - ITAutomatedPhoneControl.put_AutoStopRingOnOffHook
---

# ITAutomatedPhoneControl::put_AutoStopRingOnOffHook


## -description

The 
<b>put_AutoStopRingOnOffHook</b> method sets the <b>AutoStopRingOnOffHook</b> property. When this feature is enabled, the phone going offhook results in the termination of any incoming ring produced on the phone (via a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stopringer">ITAutomatedPhoneControl::StopRinger</a>).

## -parameters

### -param fEnabled [in]

If VARIANT_TRUE, enables automatic incoming ring termination if the phone goes offhook. If VARIANT_FALSE, disables automatic incoming ring termination if the phone goes offhook. The default value is VARIANT_TRUE.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoStopRingOnOffHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopRingOnOffHook</b> property at any time. The reconfiguration takes effect the next time the phone goes offhook.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stopringer">ITAutomatedPhoneControl::StopRinger</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autostopringonoffhook">get_AutoStopRingOnOffHook</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>