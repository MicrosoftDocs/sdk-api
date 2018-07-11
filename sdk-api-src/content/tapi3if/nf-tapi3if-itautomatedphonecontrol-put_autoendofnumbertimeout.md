---
UID: NF:tapi3if.ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout
title: ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout
author: windows-sdk-content
description: The put_AutoEndOfNumberTimeout method sets the value of the AutoEndOfNumberTimeout property. The property specifies how long to wait after a digit has been pressed before it is assumed that the entire number has been gathered.
old-location: tapi3\itautomatedphonecontrol_put_autoendofnumbertimeout.htm
old-project: tapi
ms.assetid: 985466a4-212b-48fd-b901-5fd3cc37eb0e
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],put_AutoEndOfNumberTimeout method, ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout, ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout, _tapi3_itautomatedphonecontrol_put_autoendofnumbertimeout, put_AutoEndOfNumberTimeout, put_AutoEndOfNumberTimeout method [TAPI 2.2], put_AutoEndOfNumberTimeout method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_put_autoendofnumbertimeout, tapi3if/ITAutomatedPhoneControl::put_AutoEndOfNumberTimeout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.put_AutoEndOfNumberTimeout
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a> succeeds, and detection remains suspended until the call is unselected.

The <b>AutoEndOfNumberTimeout</b> property controls only what happens after at least one keypad button has been pressed.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a>



<a href="https://msdn.microsoft.com/c5bc3176-7237-4c20-808a-b2d028ae4344">get_AutoEndOfNumberTimeout</a>
 

 

