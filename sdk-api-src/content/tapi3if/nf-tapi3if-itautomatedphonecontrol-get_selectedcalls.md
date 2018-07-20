---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_SelectedCalls
title: ITAutomatedPhoneControl::get_SelectedCalls
author: windows-sdk-content
description: The get_SelectedCalls method retrieves a VARIANT containing a pointer to a collection object indicating which calls are currently selected on this phone. See ITAutomatedPhoneControl::SelectCall for more information.
old-location: tapi3\itautomatedphonecontrol_get_selectedcalls.htm
old-project: tapi
ms.assetid: 50196789-c243-4279-8748-960898323992
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_SelectedCalls method, ITAutomatedPhoneControl.get_SelectedCalls, ITAutomatedPhoneControl::get_SelectedCalls, _tapi3_itautomatedphonecontrol_get_selectedcalls, get_SelectedCalls, get_SelectedCalls method [TAPI 2.2], get_SelectedCalls method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_selectedcalls, tapi3if/ITAutomatedPhoneControl::get_SelectedCalls
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
 - ITAutomatedPhoneControl.get_SelectedCalls
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAutomatedPhoneControl::get_SelectedCalls


## -description


The 
<b>get_SelectedCalls</b> method retrieves a VARIANT containing a pointer to a collection object indicating which calls are currently selected on this phone. See 
<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a> for more information.

This method is intended for applications written in Visual Basic, Java, or various scripting languages. C and C++ programmers should use the 
<a href="https://msdn.microsoft.com/534d453c-f47c-48e1-af59-bfa452e2d8d8">EnumerateSelectedCalls</a> method instead.


## -parameters




### -param pVariant [out]

Pointer to a VARIANT containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface pointers.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/534d453c-f47c-48e1-af59-bfa452e2d8d8">EnumerateSelectedCalls</a>



<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a>



<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

