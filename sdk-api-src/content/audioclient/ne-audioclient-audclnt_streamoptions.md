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

# AUDCLNT_STREAMOPTIONS enumeration


## -description


Defines values  that describe the characteristics of an audio stream.


## -enum-fields




### -field AUDCLNT_STREAMOPTIONS_NONE

No stream options.


### -field AUDCLNT_STREAMOPTIONS_RAW

The audio stream is a 'raw' stream that bypasses
 all signal processing except for endpoint specific,
                                  always-on processing in the Audio Processing Object (APO), driver, and hardware.



### -field AUDCLNT_STREAMOPTIONS_MATCH_FORMAT

The audio client is requesting that the audio engine match the format proposed by the client. The audio engine
will match this format only if the format is supported by                                  the audio driver and associated APOs. 



Supported in Windows 10 and later.




### -field AUDCLNT_STREAMOPTIONS_AMBISONICS




## -see-also




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>
 

 

