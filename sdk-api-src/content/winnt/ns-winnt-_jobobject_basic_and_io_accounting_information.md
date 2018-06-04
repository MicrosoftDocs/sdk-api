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

# _JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION structure


## -description


Contains basic accounting and I/O accounting information for a job object.


## -struct-fields




### -field BasicInfo

A 
<a href="https://msdn.microsoft.com/84dbe191-a5bf-4f55-815f-c4f2e60da22b">JOBOBJECT_BASIC_ACCOUNTING_INFORMATION</a> structure that specifies the basic accounting information for the job.


### -field IoInfo

An 
<a href="https://msdn.microsoft.com/78729cbe-5256-4939-a7cc-c393662f8361">IO_COUNTERS</a> structure that specifies the I/O accounting information for the job. The structure includes information for all processes that have ever been associated with the job, in addition to the information for all processes currently associated with the job.


## -see-also




<a href="https://msdn.microsoft.com/78729cbe-5256-4939-a7cc-c393662f8361">IO_COUNTERS</a>



<a href="https://msdn.microsoft.com/84dbe191-a5bf-4f55-815f-c4f2e60da22b">JOBOBJECT_BASIC_ACCOUNTING_INFORMATION</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>
 

 

