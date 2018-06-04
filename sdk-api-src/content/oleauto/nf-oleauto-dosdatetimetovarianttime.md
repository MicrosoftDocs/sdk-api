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

# DosDateTimeToVariantTime function


## -description


Converts the MS-DOS representation of time to the date and time representation stored in a variant.


## -parameters




### -param wDosDate [in]

The MS-DOS date to convert. The valid range of MS-DOS dates is January 1, 1980, to December 31, 2099, inclusive.


### -param wDosTime [in]

The MS-DOS time to convert.


### -param pvtime [out]

The converted time.


## -returns



The function returns TRUE on success and FALSE otherwise.




## -remarks



MS-DOS records file dates and times as packed 16-bit values. An MS-DOS date has the following format.

<table>
<tr>
<th>Bits</th>
<th>Contents</th>
</tr>
<tr>
<td>0–4</td>
<td>Day of the month (1–31).</td>
</tr>
<tr>
<td>5–8</td>
<td>Month (1 = January, 2 = February, and so on).</td>
</tr>
<tr>
<td>9–15</td>
<td>Year offset from 1980 (add 1980 to get the actual year).</td>
</tr>
</table>
 

An MS-DOS time has the following format.

<table>
<tr>
<th>Bits</th>
<th>Contents</th>
</tr>
<tr>
<td>0–4</td>
<td>Second divided by 2.</td>
</tr>
<tr>
<td>5–10</td>
<td>Minute (0–59).</td>
</tr>
<tr>
<td>11–15</td>
<td>Hour (0– 23 on a 24-hour clock).</td>
</tr>
</table>
 

The <b>DosDateTimeToVariantTime</b> function will accept invalid dates and try to fix them when resolving to a VARIANT time. For example, an invalid date such as 2/29/2001 will resolve to 3/1/2001. Only days are fixed, so invalid month values result in an error being returned. Days are checked to be between 1 and 31. Negative days and days greater than 31 results in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. A day equal to zero resolves as the last day of the previous month. For example, an invalid dates such as 2/0/2001 will resolve to 1/31/2001.



