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

# _MFAudioConstriction enumeration


## -description


Specifies values for audio constriction.


## -enum-fields




### -field MFaudioConstrictionOff

Audio is not constricted. 


### -field MFaudioConstriction48_16

Audio is down sampled to 48 kHz/16-bit.


### -field MFaudioConstriction44_16

Audio is down sampled to 44 kHz/16-bit.


### -field MFaudioConstriction14_14

Audio is down sampled to 14hKz/16-bit.


### -field MFaudioConstrictionMute

Audio is muted.


## -remarks



Values defined by the <b>MFAudioConstriction</b> enumeration matches the <b>EAudioConstriction</b> enumeration defined <b>audioenginebaseapo.h</b>.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

