---
UID: NS:schedule._SCHEDULE_HEADER
title: SCHEDULE_HEADER (schedule.h)
description: Used to contain the replication schedule data for a replication source.
helpviewer_keywords: ["*PSCHEDULE_HEADER","PSCHEDULE_HEADER","PSCHEDULE_HEADER structure pointer [Active Directory]","SCHEDULE_BANDWIDTH","SCHEDULE_HEADER","SCHEDULE_HEADER structure [Active Directory]","SCHEDULE_INTERVAL","SCHEDULE_PRIORITY","ad.schedule_header","schedule/PSCHEDULE_HEADER","schedule/SCHEDULE_HEADER"]
old-location: ad\schedule_header.htm
tech.root: ad
ms.assetid: 5453927e-306e-4442-a855-916005dc8e3b
ms.date: 12/05/2018
ms.keywords: '*PSCHEDULE_HEADER, PSCHEDULE_HEADER, PSCHEDULE_HEADER structure pointer [Active Directory], SCHEDULE_BANDWIDTH, SCHEDULE_HEADER, SCHEDULE_HEADER structure [Active Directory], SCHEDULE_INTERVAL, SCHEDULE_PRIORITY, ad.schedule_header, schedule/PSCHEDULE_HEADER, schedule/SCHEDULE_HEADER'
req.header: schedule.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHEDULE_HEADER
 - schedule/_SCHEDULE_HEADER
 - PSCHEDULE_HEADER
 - schedule/PSCHEDULE_HEADER
 - SCHEDULE_HEADER
 - schedule/SCHEDULE_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schedule.h
api_name:
 - SCHEDULE_HEADER
---

# SCHEDULE_HEADER structure


## -description

The <b>SCHEDULE_HEADER</b> structure is used to contain the replication schedule data for a replication source. The <a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a> structure contains an array of <b>SCHEDULE_HEADER</b> structures.

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

Contains the offset, in bytes, from the beginning of the <a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a> structure to the data for this schedule. The size and form of this data depends on the schedule type defined by the <b>Type</b> member.

## -see-also

<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>



<a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a>