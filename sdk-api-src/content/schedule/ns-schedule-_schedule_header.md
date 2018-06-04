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

# _SCHEDULE_HEADER structure


## -description


The <b>SCHEDULE_HEADER</b> structure is used to contain the replication schedule data for a replication source. The <a href="https://msdn.microsoft.com/library/windows/hardware/mt764013">SCHEDULE</a> structure contains an array of <b>SCHEDULE_HEADER</b> structures.


## -struct-fields




### -field Type

Contains one of the following values that defines the type of schedule data that is contained in this structure.



#### SCHEDULE_INTERVAL

The schedule contains a set of intervals. The <b>Offset</b> member contains the offset to an array of bytes with <b>SCHEDULE_DATA_ENTRIES</b> elements. Each byte in the array represents an hour of the week. The first hour is 00:00 on Sunday morning GMT.

Each bit of the lower four bits of each byte represents a 15 minute block within the hour that the source is available for replication. The following list lists the binary values and describes each bit of the lower four bits of the hour value.

<table>
<tr>
<th>Binary value</th>
<th>Description</th>
</tr>
<tr>
<td>
1000

</td>
<td>
The source is available for replication from 0 to 14 minutes after the hour.

</td>
</tr>
<tr>
<td>
0100

</td>
<td>
The source is available for replication from 15 to 29 minutes after the hour.

</td>
</tr>
<tr>
<td>
0010

</td>
<td>
The source is available for replication from 30 to 44 minutes after the hour.

</td>
</tr>
<tr>
<td>
0001

</td>
<td>
The source is available for replication from 45 to 59 minutes after the hour.

</td>
</tr>
</table>
 

These bits can be combined to create multiple 15 minute blocks that the source is available. For example, a binary value of 0111 indicates that the source is available from 0 to 44 minutes after the hour.

The upper fours bits of each byte are not used.



#### SCHEDULE_BANDWIDTH

Not supported.



#### SCHEDULE_PRIORITY

Not supported.


### -field Offset

Contains the offset, in bytes, from the beginning of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt764013">SCHEDULE</a> structure to the data for this schedule. The size and form of this data depends on the schedule type defined by the <b>Type</b> member.


## -see-also




<a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a>



<a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt764013">SCHEDULE</a>
 

 

