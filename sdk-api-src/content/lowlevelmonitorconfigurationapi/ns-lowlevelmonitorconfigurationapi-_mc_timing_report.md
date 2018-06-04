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

# _MC_TIMING_REPORT structure


## -description



          Contains information from a monitor's timing report.


## -struct-fields




### -field dwHorizontalFrequencyInHZ


            The monitor's horizontal synchronization frequency in Hz.
          


### -field dwVerticalFrequencyInHZ


            The monitor's vertical synchronization frequency in Hz.
          


### -field bTimingStatusByte


            Timing status byte. For more information about this value, see the Display Data Channel Command Interface (DDC/CI) standard.
          


## -see-also




<a href="https://msdn.microsoft.com/17b5a7e4-936f-451f-b586-032f94a99be5">GetTimingReport</a>



<a href="https://msdn.microsoft.com/4aca3a00-d2c6-42a6-9143-72e42c1d33bb">Monitor Configuration Structures</a>
 

 

