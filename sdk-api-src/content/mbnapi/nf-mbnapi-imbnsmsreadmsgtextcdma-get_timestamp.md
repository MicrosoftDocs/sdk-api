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

# IMbnSmsReadMsgTextCdma::get_Timestamp


## -description


The timestamp of a message.

This property is read-only.


## -parameters


## -remarks



The format of the timestamp string is "YY/MM/DD,HH:mm:SS±ZZ".

The following table defines the format of the timestamp string.


<table>
<tr>
<th>Field</th>
<th>Meaning</th>
<th>Example</th>
<th>Range</th>
</tr>
<tr>
<td>YY</td>
<td>Last 2 digits of the year</td>
<td>07 for 2007</td>
<td>00 through 99</td>
</tr>
<tr>
<td>MM</td>
<td>Month in double digits</td>
<td>01 for January</td>
<td>01 through 12</td>
</tr>
<tr>
<td>DD</td>
<td>Date in double digits</td>
<td>01 for the 1st</td>
<td>01 through 31</td>
</tr>
<tr>
<td>HH</td>
<td>Hours in 24 hour format</td>
<td>13 for 1PM</td>
<td>00 through 23</td>
</tr>
<tr>
<td>mm</td>
<td>Minutes in double digits</td>
<td>1 for 1 minute</td>
<td>00 through 59</td>
</tr>
<tr>
<td>SS</td>
<td>Seconds in double digits</td>
<td>01 for 1 second</td>
<td>00 though 59</td>
</tr>
<tr>
<td>ZZ</td>
<td>Time in relation to GMT</td>
<td>+01 for 1 hour greater</td>
<td>-12 through +13</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/d26b09f7-eb83-46ed-82cb-a702d3af5d05">IMbnSmsReadMsgTextCdma</a>
 

 

