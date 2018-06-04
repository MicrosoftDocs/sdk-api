---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a> succeeds, and detection remains suspended until the call is unselected.

The <b>AutoEndOfNumberTimeout</b> property controls only what happens after at least one keypad button has been pressed.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a>



<a href="https://msdn.microsoft.com/985466a4-212b-48fd-b901-5fd3cc37eb0e">put_AutoEndOfNumberTimeout</a>
 

 

