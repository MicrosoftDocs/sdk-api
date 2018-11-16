---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_Tone
title: ITAutomatedPhoneControl::get_Tone
author: windows-sdk-content
description: The get_Tone method returns a PHONE_TONE enum value indicating the type of tone, if any, that the phone is currently playing.
old-location: tapi3\itautomatedphonecontrol_get_tone.htm
tech.root: Tapi
ms.assetid: 62e7ae4d-7839-4568-b8b2-7a377601ea7c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_Tone method, ITAutomatedPhoneControl.get_Tone, ITAutomatedPhoneControl::get_Tone, _tapi3_itautomatedphonecontrol_get_tone, get_Tone, get_Tone method [TAPI 2.2], get_Tone method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_tone, tapi3if/ITAutomatedPhoneControl::get_Tone
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
 - ITAutomatedPhoneControl.get_Tone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITAutomatedPhoneControl.get_Tone
: 
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
 

 

