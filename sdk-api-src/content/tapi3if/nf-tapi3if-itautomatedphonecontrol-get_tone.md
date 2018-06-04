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

# ITAutomatedPhoneControl::get_Tone


## -description


The 
<b>get_Tone</b> method returns a 
<a href="https://msdn.microsoft.com/93782f7e-db48-4479-b5da-77458c41e9a6">PHONE_TONE</a> enum value indicating the type of tone, if any, that the phone is currently playing. If no tone is currently being played, the 
<b>PHONE_TONE</b> value returned is PT_SILENCE. This method has knowledge only of tones initiated by the 
<a href="https://msdn.microsoft.com/04cce8d6-ccab-4eeb-a97c-3bc24ec3fc00">StartTone</a> method on this interface.


## -parameters




### -param pTone [out]


<a href="https://msdn.microsoft.com/93782f7e-db48-4479-b5da-77458c41e9a6">PHONE_TONE</a> descriptor of tone being played.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/04cce8d6-ccab-4eeb-a97c-3bc24ec3fc00">StartTone</a>
 

 

