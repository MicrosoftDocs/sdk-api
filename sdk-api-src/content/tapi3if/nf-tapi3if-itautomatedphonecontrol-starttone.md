---
UID: NF:tapi3if.ITAutomatedPhoneControl.StartTone
title: ITAutomatedPhoneControl::StartTone (tapi3if.h)
author: windows-sdk-content
description: The StartTone method sends control tones.
old-location: tapi3\itautomatedphonecontrol_starttone.htm
tech.root: Tapi
ms.assetid: 04cce8d6-ccab-4eeb-a97c-3bc24ec3fc00
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],StartTone method, ITAutomatedPhoneControl.StartTone, ITAutomatedPhoneControl::StartTone, StartTone, StartTone method [TAPI 2.2], StartTone method [TAPI 2.2],ITAutomatedPhoneControl interface, _tapi3_itautomatedphonecontrol_starttone, tapi3.itautomatedphonecontrol_starttone, tapi3if/ITAutomatedPhoneControl::StartTone
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
ms.custom: 19H1
---

# ITAutomatedPhoneControl::StartTone


## -description


The 
<b>StartTone</b> method sends control tones.


## -parameters




### -param Tone [in]


<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_tone">PHONE_TONE</a> descriptor of the type of tone to send, such as PT_KEYPADONE.


### -param lDuration [in]

Duration, in milliseconds, of the tone being sent.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>
 

 

