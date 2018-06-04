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

# ITAutomatedPhoneControl::get_Ringer


## -description


The 
<b>get_Ringer</b> method returns a Boolean value indicating whether the phone is currently performing an incoming ring that was initiated by the 
<a href="https://msdn.microsoft.com/bf94aab7-6b12-43f8-b49f-a7cf6617dd57">StartRinger</a> method on this interface.


## -parameters




### -param pfRinging [out]

If VARIANT_TRUE, the phone is currently ringing.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/bf94aab7-6b12-43f8-b49f-a7cf6617dd57">StartRinger</a>
 

 

