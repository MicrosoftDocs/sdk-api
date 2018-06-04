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

# _MI_Interval structure


## -description


<b>MI_Interval</b> represents an interval of time.


## -struct-fields




### -field days

The number of days in the interval. (0-99999999)


### -field hours

The remaining number of hours in the interval. (0-23)


### -field minutes

The remaining number of minutes in the interval. (0-59)


### -field seconds

The remaining number of seconds in the interval. (0-59)


### -field microseconds

The remaining number of microseconds in the interval. (0-999999)


### -field __padding1

Reserved. The <b>MI_Interval</b> structure is padded to have the same size as <a href="https://msdn.microsoft.com/f06f1b0e-d21c-4b60-8099-222a1582fde1">MI_Timestamp</a>.


### -field __padding2

Reserved. The <b>MI_Interval</b> structure is padded to have the same size as <a href="https://msdn.microsoft.com/f06f1b0e-d21c-4b60-8099-222a1582fde1">MI_Timestamp</a>.


### -field __padding3

Reserved. The <b>MI_Interval</b> structure is padded to have the same size as <a href="https://msdn.microsoft.com/f06f1b0e-d21c-4b60-8099-222a1582fde1">MI_Timestamp</a>.

