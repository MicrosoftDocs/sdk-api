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

# SYSTEM_POWER_CONDITION enumeration


## -description


Used by the <b>GUID_ACDC_POWER_SOURCE</b> power event to indicate the current 
    power source.


## -enum-fields




### -field PoAc

The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive 
      adapter).


### -field PoDc

The system is receiving power from built-in batteries.


### -field PoHot

The computer is powered by a short-term power source such as a UPS device.


### -field PoConditionMaximum

Values equal to or greater than this value indicate an out of range value.


## -see-also




<a href="https://msdn.microsoft.com/f78cd97f-586f-4091-ab4a-5f109a0f679a">Power Management Enumeration Types</a>
 

 

