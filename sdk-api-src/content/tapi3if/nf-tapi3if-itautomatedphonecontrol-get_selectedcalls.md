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
 

 

