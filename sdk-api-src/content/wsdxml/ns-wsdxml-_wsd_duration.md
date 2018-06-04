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

# _WSD_DURATION structure


## -description


Represents a length of time.


## -struct-fields




### -field isPositive

This parameter is <b>TRUE</b> if the entire duration is positive.


### -field year

The year value. This number is a value between 0 and max(ULONG).


### -field month

The month value. This number is a value between 0 and max(ULONG).


### -field day

The day value. This number is a value between 0 and max(ULONG).


### -field hour

The hour value. This number is a value between 0 and max(ULONG).


### -field minute

The minute value. This number is a value between 0 and max(ULONG).


### -field second

The second value. This number is a value between 0 and max(ULONG).


### -field millisecond

The millisecond value (0-999).


## -remarks



If any numeric member has a value of 0, then the member and its value is not included in the XML output when the structure is converted to XML.



