---
UID: NF:tapi3if.ITAutomatedPhoneControl.EnumerateSelectedCalls
title: ITAutomatedPhoneControl::EnumerateSelectedCalls
author: windows-sdk-content
description: The EnumerateSelectedCalls method retrieves an enumerator object indicating which calls are currently selected on this phone. See ITAutomatedPhoneControl::SelectCall for more information.
old-location: tapi3\itautomatedphonecontrol_enumerateselectedcalls.htm
tech.root: tapi
ms.assetid: 534d453c-f47c-48e1-af59-bfa452e2d8d8
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: EnumerateSelectedCalls, EnumerateSelectedCalls method [TAPI 2.2], EnumerateSelectedCalls method [TAPI 2.2],ITAutomatedPhoneControl interface, ITAutomatedPhoneControl interface [TAPI 2.2],EnumerateSelectedCalls method, ITAutomatedPhoneControl.EnumerateSelectedCalls, ITAutomatedPhoneControl::EnumerateSelectedCalls, _tapi3_itautomatedphonecontrol_enumerateselectedcalls, tapi3.itautomatedphonecontrol_enumerateselectedcalls, tapi3if/ITAutomatedPhoneControl::EnumerateSelectedCalls
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.EnumerateSelectedCalls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::EnumerateSelectedCalls


## -description


The 
<b>EnumerateSelectedCalls</b> method retrieves an enumerator object indicating which calls are currently selected on this phone. See 
<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a> for more information.

This method is intended for C and C++ programmers. Applications written in Visual Basic, Java, or various scripting languages should use the 
<a href="https://msdn.microsoft.com/50196789-c243-4279-8748-960898323992">get_SelectedCalls</a> method instead.


## -parameters




### -param ppCallEnum [out]

Pointer to the 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface returned by this method. The application must call the <b>Release</b> method on the 
<b>IEnumCall</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a>
 

 

