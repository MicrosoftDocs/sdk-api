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

# ISchedule interface


## -description


Specifies when the data collector set runs.

To get this interface, call the <a href="https://msdn.microsoft.com/8fa10cd9-d1ae-47c7-80e2-416165164491">IScheduleCollection::CreateSchedule</a> method.


## -remarks



To create the object from a script, use the Pla.Schedule program identifier.

PLA uses the schedule when the <a href="https://msdn.microsoft.com/75ebe328-1494-464c-9491-e8a39e1d8ee1">IDataCollectorSet::SchedulesEnabled</a> property is VARIANT_TRUE.

For an example that shows the XML that you can use to initialize this object if you call the <a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">IDataCollectorSet::SetXml</a> method, see the Remarks section of <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>.  When you specify the XML to create the object, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements. 



