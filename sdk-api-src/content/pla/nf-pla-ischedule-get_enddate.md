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

# ISchedule::get_EndDate


## -description


Retrieves or sets the last date that the schedule is valid.

This property is read/write.


## -parameters


## -remarks



The end date must be greater than or equal to the start date.

The set cannot be started after the end date, but if the set is running when the end date is reached, it continues to run.




## -see-also




<a href="https://msdn.microsoft.com/b02043c6-5010-45a1-a4a4-ce30cbf0dba0">ISchedule</a>



<a href="https://msdn.microsoft.com/1bb90c84-0249-4714-9371-d2aed2922d9b">ISchedule::StartDate</a>
 

 

