---
UID: NF:fsrmreports.IFsrmReportJob.Run
title: IFsrmReportJob::Run
author: windows-sdk-content
description: Runs all the reports in the job.
old-location: fsrm\ifsrmreportjob_run.htm
old-project: Fsrm
ms.assetid: 74f369d1-2e3d-49a5-bf54-c1b7c13efbd7
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],Run method, IFsrmReportJob.Run, IFsrmReportJob::Run, Run, Run method [File Server Resource Manager], Run method [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_run, fsrm.ifsrmreportjob_run, fsrmreports/IFsrmReportJob::Run
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportJob.Run
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

