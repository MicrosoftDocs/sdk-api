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

# TAPI_DETECTTONE structure


## -description


The 
<b>TAPI_DETECTTONE</b> structure describes a tone to be monitored. This is used as an entry in an array.


## -struct-fields




### -field dwAppSpecific

Used by the application for tagging the tone. When this tone is detected, the value of the <b>dwAppSpecific</b> member is passed back to the application.


### -field dwDuration

The duration, in milliseconds, during which the tone should be present before a detection is made.


### -field dwFrequency1

The frequency, in hertz, of a component of the tone.


### -field dwFrequency2

The frequency, in hertz, of a component of the tone.


### -field dwFrequency3

The frequency, in hertz, of a component of the tone. If fewer than three frequencies are needed in the tone, a value of zero should be used for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be used for silence detection.


## -see-also




<a href="https://msdn.microsoft.com/e059bfc0-3701-4e07-8c30-0a2512731080">ITLegacyCallMediaControl2::DetectTones</a>



<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">ITLegacyCallMediaControl2::DetectTonesByCollection</a>



<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a>
 

 

