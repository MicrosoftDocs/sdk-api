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

# _STRING_COUNTER_HEADER structure


## -description


Indicates where in the <a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block that the string that contains the name or help string  for the indicated performance counter starts. The <b>PERF_STRING_COUNTER_HEADER</b> structure is part of the
<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block


## -struct-fields




### -field dwCounterId

The identifier of the  performance counter.


### -field dwOffset

The number of bytes from the start of the
<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block to the null-terminated UTF-16LE data. A value of 0xFFFFFFFF indicates that the string is not present; in other words, that the value of the string is NULL.


## -remarks



The <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to
<b>PERF_REG_COUNTER_NAME_STRINGS</b> or <b>PERF_REG_COUNTER_HELP_STRINGS</b> gets a
<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block that contains one or more
<b>PERF_STRING_COUNTER_HEADER</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a>



<a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a>
 

 

