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
 

 

