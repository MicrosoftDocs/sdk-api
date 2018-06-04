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

# DIOBJECTATTRIBUTES structure


## -description


The DIOBJECTATTRIBUTES structure describes the information contained in the "Attributes" value of the registry key for each "object" on a device. If the "Attributes" value is absent, then default attributes are used. 


## -struct-fields




### -field dwFlags

 There may be zero, one, or more of the following flags: 





#### DIDOI_FFACTUATOR

Indicates that the object can have force feedback effects applied to it. 



#### DIDOI_FFEFFECTTRIGGER

Indicates that the object can trigger playback of force feedback effects. 



#### DIDOI_ASPECTPOSITION

Indicates that the object reports position information. 



#### DIDOI_ASPECTVELOCITY

Indicates that the object reports velocity information. 



#### DIDOI_ASPECTACCEL

Indicates that the object reports acceleration information. 



#### DIDOI_ASPECTFORCE

Indicates that the object reports force information. 



#### DIDOI_ASPECTMASK

Indicates the bits that are used to report aspect information. An object can represent, at most, one aspect. 



#### DIDOI_POLLED

Indicates that the object must be explicitly polled in order for data to be retrieved from it. If this flag is not set, then data for the object is interrupt-driven. 


### -field wUsagePage

Specifies the HID usage page to associate with the object. 


### -field wUsage

Specifies the HID usage to associate with the object. 

