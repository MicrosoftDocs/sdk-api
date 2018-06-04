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

# eAVEncDDService enumeration


## -description



Specifies the audio service contained in a Dolby Digital audio stream. This enumeration is used with the <a href="https://msdn.microsoft.com/454021c7-f574-443c-bd23-411be44162b5">AVEncDDService</a> property.




## -enum-fields




### -field eAVEncDDService_CM

Complete main audio service.


### -field eAVEncDDService_ME

Main service: music and effects. (The main audio service minus the dialog channel.)


### -field eAVEncDDService_VI

Associated service: visually impaired.


### -field eAVEncDDService_HI

Associated service: hard of hearing.


### -field eAVEncDDService_D

Associated service: dialog.


### -field eAVEncDDService_C

Associated service: commentary.


### -field eAVEncDDService_E

Associated service: emergency.


### -field eAVEncDDService_VO

Associated service: voice over.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

