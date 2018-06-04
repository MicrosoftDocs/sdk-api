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

# _JOBOBJECT_BASIC_PROCESS_ID_LIST structure


## -description


Contains the process identifier list for a job object. If the job is nested, the process identifier list consists of all processes associated with the job and its child jobs.


## -struct-fields




### -field NumberOfAssignedProcesses

The number of process identifiers to be stored in <b>ProcessIdList</b>.


### -field NumberOfProcessIdsInList

The number of process identifiers returned in the <b>ProcessIdList</b> buffer. If this number is less than <b>NumberOfAssignedProcesses</b>, increase the size of the buffer to accommodate the complete list.


### -field ProcessIdList

A variable-length array of process identifiers returned by this call. Array elements 0 through <b>NumberOfProcessIdsInList</b>
						– 1 contain valid process identifiers.


## -see-also




<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

