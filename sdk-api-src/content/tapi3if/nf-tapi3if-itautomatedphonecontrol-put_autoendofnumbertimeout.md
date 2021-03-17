---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout
title: ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout (tapi3if.h)
description: The put_AutoEndOfNumberTimeout method sets the value of the AutoEndOfNumberTimeout property. The property specifies how long to wait after a digit has been pressed before it is assumed that the entire number has been gathered.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","put_AutoEndOfNumberTimeout method","ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout","ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout","_tapi3_itautomatedphonecontrol_put_autoendofnumbertimeout","put_AutoEndOfNumberTimeout","put_AutoEndOfNumberTimeout method [TAPI 2.2]","put_AutoEndOfNumberTimeout method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_put_autoendofnumbertimeout","tapi3if/ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout"]
old-location: tapi3\itautomatedphonecontrol_put_autoendofnumbertimeout.htm
tech.root: tapi3
ms.assetid: 985466a4-212b-48fd-b901-5fd3cc37eb0e
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoEndOfNumberTimeout method, ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout, ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout, _tapi3_itautomatedphonecontrol_put_autoendofnumbertimeout, put_AutoEndOfNumberTimeout, put_AutoEndOfNumberTimeout method [TAPI 2.2], put_AutoEndOfNumberTimeout method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autoendofnumbertimeout, tapi3if/ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout
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
 - ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout
 - tapi3if/ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout
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
 - ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout
---

# ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout


## -description

The 
<b>put_AutoEndOfNumberTimeout</b> method sets the value of the <b>AutoEndOfNumberTimeout</b> property. The property specifies how long to wait after a digit has been pressed before it is assumed that the entire number has been gathered.

## -parameters

### -param lTimeout [in]

Timeout interval to wait, in milliseconds (ms). The default value is 3000 ms.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

A value of 0 turns off this timeout and bases the end-of-number detection solely on the user pressing the # or SEND buttons.

End-of-number-detection ceases (without a detection event) when an invocation of 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a> succeeds, and detection remains suspended until the call is unselected.

The <b>AutoEndOfNumberTimeout</b> property controls only what happens after at least one keypad button has been pressed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autoendofnumbertimeout">get_AutoEndOfNumberTimeout</a>