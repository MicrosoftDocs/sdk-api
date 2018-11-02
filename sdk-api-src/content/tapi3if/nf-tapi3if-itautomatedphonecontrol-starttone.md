---
UID: NF:tapi3if.ITAutomatedPhoneControl.StartTone
title: ITAutomatedPhoneControl::StartTone
author: windows-sdk-content
description: The StartTone method sends control tones.
old-location: tapi3\itautomatedphonecontrol_starttone.htm
tech.root: tapi
ms.assetid: 04cce8d6-ccab-4eeb-a97c-3bc24ec3fc00
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],StartTone method, ITAutomatedPhoneControl.StartTone, ITAutomatedPhoneControl::StartTone, StartTone, StartTone method [TAPI 2.2], StartTone method [TAPI 2.2],ITAutomatedPhoneControl interface, _tapi3_itautomatedphonecontrol_starttone, tapi3.itautomatedphonecontrol_starttone, tapi3if/ITAutomatedPhoneControl::StartTone
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
 - ITAutomatedPhoneControl.StartTone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::StartTone


## -description


The 
<b>StartTone</b> method sends control tones.


## -parameters




### -param Tone [in]


<a href="https://msdn.microsoft.com/93782f7e-db48-4479-b5da-77458c41e9a6">PHONE_TONE</a> descriptor of the type of tone to send, such as PT_KEYPADONE.


### -param lDuration [in]

Duration, in milliseconds, of the tone being sent.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>
 

 

