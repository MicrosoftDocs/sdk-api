---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_AutoEndOfNumberTimeout
title: ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout (tapi3if.h)
description: The get_AutoEndOfNumberTimeout method retrieves the current value of the AutoEndOfNumberTimeout property. The property specifies how long to wait after a digit has been pressed before it is assumed that the entire number has been gathered.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_AutoEndOfNumberTimeout method","ITAutomatedPhoneControl.get_AutoEndOfNumberTimeout","ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout","_tapi3_itautomatedphonecontrol_get_autoendofnumbertimeout","get_AutoEndOfNumberTimeout","get_AutoEndOfNumberTimeout method [TAPI 2.2]","get_AutoEndOfNumberTimeout method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_autoendofnumbertimeout","tapi3if/ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout"]
old-location: tapi3\itautomatedphonecontrol_get_autoendofnumbertimeout.htm
tech.root: tapi3
ms.assetid: c5bc3176-7237-4c20-808a-b2d028ae4344
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_AutoEndOfNumberTimeout method, ITAutomatedPhoneControl.get_AutoEndOfNumberTimeout, ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout, _tapi3_itautomatedphonecontrol_get_autoendofnumbertimeout, get_AutoEndOfNumberTimeout, get_AutoEndOfNumberTimeout method [TAPI 2.2], get_AutoEndOfNumberTimeout method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_autoendofnumbertimeout, tapi3if/ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout
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
 - ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout
 - tapi3if/ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout
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
 - ITAutomatedPhoneControl.get_AutoEndOfNumberTimeout
---

# ITAutomatedPhoneControl::get_AutoEndOfNumberTimeout


## -description

The 
<b>get_AutoEndOfNumberTimeout</b> method retrieves the current value of the <b>AutoEndOfNumberTimeout</b> property. The property specifies how long to wait after a digit has been pressed before it is assumed that the entire number has been gathered.

## -parameters

### -param plTimeout [out]

Time-out interval to wait, in milliseconds (ms). The default value is 3000 ms.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

A value of 0 turns off this timeout and bases the end-of-number detection solely on the user pressing the # or SEND button.

End-of-number-detection ceases (without a detection event) when an invocation of 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a> succeeds, and detection remains suspended until the call is unselected.

The <b>AutoEndOfNumberTimeout</b> property controls only what happens after at least one keypad button has been pressed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autoendofnumbertimeout">put_AutoEndOfNumberTimeout</a>