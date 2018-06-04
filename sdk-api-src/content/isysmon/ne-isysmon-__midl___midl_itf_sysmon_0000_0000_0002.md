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

# __MIDL___MIDL_itf_sysmon_0000_0000_0002 enumeration


## -description


Determines the type of data to return from a given data point on the graph.


## -enum-fields




### -field sysmonDataAvg

Average value of the counter.


### -field sysmonDataMin

Minimum value of the counter.


### -field sysmonDataMax

Maximum value of the counter.


### -field sysmonDataTime

Date and time that the counter value was collected. If SYSMON compresses more than one sample into the counter value, the date and time are from the last sample.


### -field sysmonDataCount

Number of samples that were compressed into the data point.


## -see-also




<a href="https://msdn.microsoft.com/e8484301-4575-41ee-9c6d-a454eca0e82d">CounterItem.GetDataAt</a>
 

 

