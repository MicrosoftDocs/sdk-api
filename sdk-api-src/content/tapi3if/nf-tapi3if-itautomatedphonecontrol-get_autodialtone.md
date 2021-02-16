---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoDialtone
title: ITAutomatedPhoneControl::get_AutoDialtone (tapi3if.h)
description: The get_AutoDialtone method retrieves the current value of the AutoDialtone property.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoDialtone method","ITAutomatedPhoneControl.get_AutoDialtone","ITAutomatedPhoneControl::get_AutoDialtone","_tapi3_itautomatedphonecontrol_get_autodialtone","get_AutoDialtone","get_AutoDialtone method [TAPI 2.2]","get_AutoDialtone method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autodialtone","tapi3if/ITAutomatedPhoneControl::get_AutoDialtone"]
old-location: tapi3\itautomatedphonecontrol_get_autodialtone.htm
tech.root: tapi3
ms.assetid: 977be70d-bb2d-490a-afd1-8e7f496b10ae
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoDialtone method, ITAutomatedPhoneControl.get_AutoDialtone, ITAutomatedPhoneControl::get_AutoDialtone, _tapi3_itautomatedphonecontrol_get_autodialtone, get_AutoDialtone, get_AutoDialtone method [TAPI 2.2], get_AutoDialtone method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autodialtone, tapi3if/ITAutomatedPhoneControl::get_AutoDialtone
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
 - ITAutomatedPhoneControl::get_AutoDialtone
 - tapi3if/ITAutomatedPhoneControl::get_AutoDialtone
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
 - ITAutomatedPhoneControl.get_AutoDialtone
---

# ITAutomatedPhoneControl::get_AutoDialtone


## -description

The 
<b>get_AutoDialtone</b> method retrieves the current value of the <b>AutoDialtone</b> property. When this feature is enabled, the phone going offhook results in a dial tone produced on the audio render device associated with the phone. No dial tone is produced if the phone was ringing when it went offhook.

## -parameters

### -param pfEnabled [out]

If VARIANT_TRUE, auto dial tone is enabled. If VARIANT_FALSE, auto dial tone is disabled.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The <b>AutoDialtone</b> property functions only when the value of the <b>PhoneHandlingEnabled</b> property is VARIANT_TRUE. You can set the <b>AutoDialtone</b> property at any time. The reconfiguration takes effect the next time the phone goes offhook.

All dial tone generation ceases when an invocation of 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a> succeeds; dial tone generation remains suspended until the call is unselected.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autodialtone">put_AutoDialtone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>