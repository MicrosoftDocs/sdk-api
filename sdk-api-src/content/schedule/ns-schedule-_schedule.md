---
UID: NS:schedule._SCHEDULE
title: "_SCHEDULE"
author: windows-sdk-content
description: Used with the DsReplicaAdd and DsReplicaModify functions to contain replication schedule data for a replication source.
old-location: ad\schedule.htm
tech.root: AD
ms.assetid: d86890db-b34a-415a-820a-6d4790914218
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSCHEDULE, PSCHEDULE, PSCHEDULE structure pointer [Active Directory], SCHEDULE, SCHEDULE structure [Active Directory], _SCHEDULE, ad.schedule, schedule/PSCHEDULE, schedule/SCHEDULE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schedule.h
api_name:
 - SCHEDULE
product: Windows
targetos: Windows
req.typenames: SCHEDULE, *PSCHEDULE
req.redist: 
---

# _SCHEDULE structure


## -description


The <b>SCHEDULE</b> structure is a variable-length structure used with the <a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a> and <a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a> functions to contain replication schedule data for a replication source.


## -struct-fields




### -field Size

Contains the size, in bytes, of the <b>SCHEDULE</b> structure, including the size of all of the elements and data of the <b>Schedules</b> array.


### -field Bandwidth

Not used.


### -field NumberOfSchedules

Contains the number of elements in the <b>Schedules</b> array.


### -field Schedules

Contains an array of <a href="https://msdn.microsoft.com/5453927e-306e-4442-a855-916005dc8e3b">SCHEDULE_HEADER</a> structures that contain the replication schedule data for the replication source. The <b>NumberOfSchedules</b> member contains the number of elements in this array. Currently, this array can only contain one element.


## -see-also




<a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a>



<a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a>



<a href="https://msdn.microsoft.com/5453927e-306e-4442-a855-916005dc8e3b">SCHEDULE_HEADER</a>
 

 

