---
UID: NF:fsrmreports.IFsrmFileManagementJob.Run
title: IFsrmFileManagementJob::Run
author: windows-sdk-content
description: Runs the job.
old-location: fsrm\ifsrmfilemanagementjob_run.htm
tech.root: fsrm
ms.assetid: 2db27e05-5c3b-4827-a616-36fd46281911
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],Run method, IFsrmFileManagementJob.Run, IFsrmFileManagementJob::Run, Run, Run method [File Server Resource Manager], Run method [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_run, fsrm.ifsrmfilemanagementjob_run, fsrmreports/IFsrmFileManagementJob::Run
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJob.Run
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::Run


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Runs the job.


## -parameters




### -param context [in]

Specifies to which subdirectory the reports or logging are written, if enabled. For possible values, see 
      the <a href="https://msdn.microsoft.com/02e18cc2-7c5e-473f-8a7f-e310bfb1c57d">FsrmReportGenerationContext</a> 
      enumeration.


## -returns



The method returns the following return values.




## -remarks



Since the file management job consumes the results of classification, running the file management job also 
    runs classification.

The jobs are run asynchronously. Jobs that run in the scheduled context remain in the queue for five minutes 
    before they are run; jobs that run in the other contexts remain in the queue for 30 seconds. To block your code 
    until the job completes, calling the 
    <a href="https://msdn.microsoft.com/8d0d0046-989f-4d6a-b9da-caf6df44e1db">IFsrmFileManagementJob::WaitForCompletion</a> 
    method. Calling <b>WaitForCompletion</b> 
    removes the job from the queue and runs it immediately.

If you call this method and the job is already queued or running, the method returns an error. To determine 
    the status of the job, access the 
    <a href="https://msdn.microsoft.com/ae87183c-8e82-487c-b774-6b2b802fa645">IFsrmReportJob::RunningStatus</a> 
    property.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

