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

# _MFCLOCK_STATE enumeration


## -description



Defines the state of a clock.




## -enum-fields




### -field MFCLOCK_STATE_INVALID

The clock is invalid. A clock might be invalid for several reasons. Some clocks return this state before the first start. This state can also occur if the underlying device is lost.


### -field MFCLOCK_STATE_RUNNING

The clock is running. While the clock is running, the time advances at the clock's frequency and current rate.


### -field MFCLOCK_STATE_STOPPED

The clock is stopped. While stopped, the clock reports a time of 0.


### -field MFCLOCK_STATE_PAUSED

The clock is paused. While paused, the clock reports the time it was paused.


## -see-also




<a href="https://msdn.microsoft.com/8e2dda03-f589-4572-b715-2be7b29a6ace">IMFClock::GetState</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

