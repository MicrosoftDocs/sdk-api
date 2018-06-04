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

# IFsrmReportJob::Run


## -description


Runs all the reports in the job.


## -parameters




### -param context [in]

Specifies to which subdirectory the reports are written. For possible values, see the <a href="https://msdn.microsoft.com/02e18cc2-7c5e-473f-8a7f-e310bfb1c57d">FsrmReportGenerationContext</a> enumeration.


## -returns



The method returns the following return values.




## -remarks



Note that reports that run in the scheduled context remain in the queue for five minutes before they are run; reports that run in the other contexts remain in the queue for 30 seconds.

If you call this method and the report job is already queued or running, the method returns an error. To determine the status of the job, access the <a href="https://msdn.microsoft.com/ae87183c-8e82-487c-b774-6b2b802fa645">IFsrmReportJob::RunningStatus</a> property.


#### Examples

For an example,  see <a href="https://msdn.microsoft.com/8087542d-5873-414b-8903-544c2e57cba1">Running a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>



<a href="https://msdn.microsoft.com/127027a0-7f05-4de4-a3be-8e3c3ec30910">IFsrmReportJob::WaitForCompletion</a>
 

 

