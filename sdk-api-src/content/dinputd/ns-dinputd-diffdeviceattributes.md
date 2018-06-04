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

# DIFFDEVICEATTRIBUTES structure


## -description


The DIFFDEVICEATTRIBUTES structure describes the information contained in the "Attributes" value of the <b>OEMForceFeedback</b> registry key. 


## -struct-fields




### -field dwFlags

Reserved for future use. This member must be set to zero. 


### -field dwFFSamplePeriod

Specifies the minimum time between playback of force commands, in microseconds. 


### -field dwFFMinTimeResolution

Specifies the minimum amount of time that the device can resolve, in microseconds. The device rounds any time values to the nearest supported increment. For example, if the value of <b>dwFFMinTimeResolution</b> is 1000, then the device would round any times to the nearest millisecond. 

