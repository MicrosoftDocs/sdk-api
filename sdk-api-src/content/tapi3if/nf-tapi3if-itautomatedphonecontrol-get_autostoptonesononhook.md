---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook
title: ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook (tapi3if.h)
description: The get_AutoStopTonesOnOnHook method retrieves the current value of the AutoStopTonesOnOnHook property.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoStopTonesOnOnHook method","ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook","ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook","_tapi3_itautomatedphonecontrol_get_autostoptonesononhook","get_AutoStopTonesOnOnHook","get_AutoStopTonesOnOnHook method [TAPI 2.2]","get_AutoStopTonesOnOnHook method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autostoptonesononhook","tapi3if/ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook"]
old-location: tapi3\itautomatedphonecontrol_get_autostoptonesononhook.htm
tech.root: tapi3
ms.assetid: 2ece8d7a-b280-42b6-9f51-d88650488699
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoStopTonesOnOnHook method, ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook, ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook, _tapi3_itautomatedphonecontrol_get_autostoptonesononhook, get_AutoStopTonesOnOnHook, get_AutoStopTonesOnOnHook method [TAPI 2.2], get_AutoStopTonesOnOnHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autostoptonesononhook, tapi3if/ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook
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
 - ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook
 - tapi3if/ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook
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
 - ITAutomatedPhoneControl.get_AutoStopTonesOnOnHook
---

# ITAutomatedPhoneControl::get_AutoStopTonesOnOnHook


## -description

The 
<b>get_AutoStopTonesOnOnHook</b> method retrieves the current value of the <b>AutoStopTonesOnOnHook</b> property. When this feature is enabled, the phone going onhook results in the termination of any tone produced on the audio render device associated with the phone (via a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">ITAutomatedPhoneControl::StopTone</a>).

## -parameters

### -param pfEnabled [out]

If VARIANT_TRUE, automatic stop of tone generation upon onhook is enabled. If VARIANT_FALSE, automatic stop of tone generation upon onhook is disabled.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoStopTonesOnOnHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopTonesOnOnHook</b> property at any time. The reconfiguration takes effect the next time the phone goes onhook.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">ITAutomatedPhoneControl::StopTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autostoptonesononhook">put_AutoStopTonesOnOnHook</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>