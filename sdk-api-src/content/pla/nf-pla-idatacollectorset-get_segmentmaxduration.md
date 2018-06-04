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

# IDataCollectorSet::get_SegmentMaxDuration


## -description


Retrieves or sets the duration that the data collector set can run before it begins writing to new log files.

This property is read/write.


## -parameters


## -remarks



You must enable the <a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a> property for this property to take effect.

This duration needs to be less than the <a href="https://msdn.microsoft.com/afa8f8f2-52a7-481f-ba7e-19f9b757aeb8">IDataCollectorSet::Duration</a> or <a href="https://msdn.microsoft.com/80a5c1a9-2d0a-4700-824b-1333b5c7c374">ISchedule::EndDate</a> property.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/afa8f8f2-52a7-481f-ba7e-19f9b757aeb8">IDataCollectorSet::Duration</a>



<a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a>



<a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a>
 

 

