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

# _MFCLOCK_CHARACTERISTICS_FLAGS enumeration


## -description


Contains flags that describe the characteristics of a clock. These flags are returned by the <a href="https://msdn.microsoft.com/50a81e8b-9aa8-484c-afb7-950068feefc4">IMFClock::GetClockCharacteristics</a> method.


## -enum-fields




### -field MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ

The clock times returned by the <a href="https://msdn.microsoft.com/0a897426-d994-4b27-9f13-9b0c7c9b3a9b">IMFClock::GetCorrelatedTime</a> method are in units of 100 nanoseconds. If this flag is absent, call <a href="https://msdn.microsoft.com/9dfc0efc-d274-45a6-b1ab-30f6215fbed8">IMFClock::GetProperties</a> to get the clock frequency. The clock frequency is given in the <b>qwClockFrequency</b> member of the <a href="https://msdn.microsoft.com/1efc6602-9851-40e5-85aa-0335d4e899a2">MFCLOCK_PROPERTIES</a> structure returned by that method.


### -field MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING

The clock is always running. If this flag is present, the clock cannot be paused or stopped. If this flag is absent, call the <a href="https://msdn.microsoft.com/8e2dda03-f589-4572-b715-2be7b29a6ace">IMFClock::GetState</a> method to get the current state.


### -field MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK

The clock times are generated from the system clock.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

