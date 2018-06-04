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

# CoDosDateTimeToFileTime function


## -description


Converts the MS-DOS representation of the time and date to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure used by Windows.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters




### -param nDosDate [in]

The MS-DOS date.


### -param nDosTime [in]

The MS-DOS time.


### -param lpFileTime [out]

A pointer to the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>, probably because of invalid arguments.




## -remarks



 An MS-DOS date has the following format.

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Days of the month (1-31).
</td>
</tr>
<tr>
<td>5-8</td>
<td>Months (1 = January, 2 = February, and so forth). 
</td>
</tr>
<tr>
<td>9-15</td>
<td>Year offset from 1980 (add 1980 to get actual year). 
</td>
</tr>
</table>
 

An MS-DOS time has the following format.

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Seconds divided by 2.</td>
</tr>
<tr>
<td>5-10</td>
<td>Minutes (0-59).
</td>
</tr>
<tr>
<td>11-15</td>
<td>Hours (0-23 on a 24-hour clock). 
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00083429-1d61-4a0b-bb73-82158869466d">CoFileTimeNow</a>



<a href="https://msdn.microsoft.com/38670fe7-10cf-44e2-a5f1-60ec43fd83b5">CoFileTimeToDosDateTime</a>
 

 

