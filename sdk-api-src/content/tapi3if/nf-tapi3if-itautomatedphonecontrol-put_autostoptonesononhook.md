---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook
title: ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook (tapi3if.h)
description: The put_AutoStopTonesOnOnHook method sets the AutoStopTonesOnOnHook property for this phone.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoStopTonesOnOnHook method","ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook","ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook","_tapi3_itautomatedphonecontrol_put_autostoptonesononhook","put_AutoStopTonesOnOnHook","put_AutoStopTonesOnOnHook method [TAPI 2.2]","put_AutoStopTonesOnOnHook method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autostoptonesononhook","tapi3if/ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook"]
old-location: tapi3\itautomatedphonecontrol_put_autostoptonesononhook.htm
tech.root: tapi3
ms.assetid: 0047b631-91fc-47fb-aa38-cedb096a5646
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoStopTonesOnOnHook method, ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook, ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook, _tapi3_itautomatedphonecontrol_put_autostoptonesononhook, put_AutoStopTonesOnOnHook, put_AutoStopTonesOnOnHook method [TAPI 2.2], put_AutoStopTonesOnOnHook method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autostoptonesononhook, tapi3if/ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook
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
 - ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook
 - tapi3if/ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook
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
 - ITAutomatedPhoneControl.put_AutoStopTonesOnOnHook
---

# ITAutomatedPhoneControl::put_AutoStopTonesOnOnHook


## -description

The 
<b>put_AutoStopTonesOnOnHook</b> method sets the <b>AutoStopTonesOnOnHook</b> property for this phone. When this feature is enabled, the phone going onhook results in the termination of any tone produced on the audio render device associated with the phone (via a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">ITAutomatedPhoneControl::StopTone</a>).

## -parameters

### -param fEnabled [in]

If VARIANT_TRUE, enables automatic stop of tone generation if the phone goes onhook. If VARIANT_FALSE, disables automatic stop if the phone goes onhook. The default value is VARIANT_TRUE.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoStopTonesOnOnHook</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoStopTonesOnOnHook</b> property at any time. The reconfiguration takes effect the next time the phone goes onhook.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">ITAutomatedPhoneControl::StopTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autostoptonesononhook">get_AutoStopTonesOnOnHook</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>