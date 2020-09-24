---
UID: NS:schedule._SCHEDULE
title: SCHEDULE (schedule.h)
description: Used with the DsReplicaAdd and DsReplicaModify functions to contain replication schedule data for a replication source.
helpviewer_keywords: ["*PSCHEDULE","PSCHEDULE","PSCHEDULE structure pointer [Active Directory]","SCHEDULE","SCHEDULE structure [Active Directory]","ad.schedule","schedule/PSCHEDULE","schedule/SCHEDULE"]
old-location: ad\schedule.htm
tech.root: ad
ms.assetid: d86890db-b34a-415a-820a-6d4790914218
ms.date: 12/05/2018
ms.keywords: '*PSCHEDULE, PSCHEDULE, PSCHEDULE structure pointer [Active Directory], SCHEDULE, SCHEDULE structure [Active Directory], ad.schedule, schedule/PSCHEDULE, schedule/SCHEDULE'
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
req.typenames: SCHEDULE, *PSCHEDULE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHEDULE
 - schedule/_SCHEDULE
 - PSCHEDULE
 - schedule/PSCHEDULE
 - SCHEDULE
 - schedule/SCHEDULE
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
 - SCHEDULE
---

# SCHEDULE structure


## -description

The <b>SCHEDULE</b> structure is a variable-length structure used with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a> functions to contain replication schedule data for a replication source.

## -struct-fields

### -field Size

Contains the size, in bytes, of the <b>SCHEDULE</b> structure, including the size of all of the elements and data of the <b>Schedules</b> array.

### -field Bandwidth

Not used.

### -field NumberOfSchedules

Contains the number of elements in the <b>Schedules</b> array.

### -field Schedules

Contains an array of <a href="/windows/desktop/api/schedule/ns-schedule-schedule_header">SCHEDULE_HEADER</a> structures that contain the replication schedule data for the replication source. The <b>NumberOfSchedules</b> member contains the number of elements in this array. Currently, this array can only contain one element.

## -see-also

<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>



<a href="/windows/desktop/api/schedule/ns-schedule-schedule_header">SCHEDULE_HEADER</a>