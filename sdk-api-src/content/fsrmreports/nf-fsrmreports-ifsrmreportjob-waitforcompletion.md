---
UID: NF:fsrmreports.IFsrmReportJob.WaitForCompletion
title: IFsrmReportJob::WaitForCompletion
author: windows-sdk-content
description: Waits for the reports in the job to complete.
old-location: fsrm\ifsrmreportjob_waitforcompletion.htm
old-project: Fsrm
ms.assetid: 127027a0-7f05-4de4-a3be-8e3c3ec30910
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],WaitForCompletion method, IFsrmReportJob.WaitForCompletion, IFsrmReportJob::WaitForCompletion, WaitForCompletion, WaitForCompletion method [File Server Resource Manager], WaitForCompletion method [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_waitforcompletion, fsrm.ifsrmreportjob_waitforcompletion, fsrmreports/IFsrmReportJob::WaitForCompletion
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
 - IFsrmReportJob.WaitForCompletion
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportJob::WaitForCompletion


## -description


Waits for the reports in the job to complete.


## -parameters




### -param waitSeconds [in]

The number of seconds to wait for the reports to complete. The method returns when the period expires or the reports complete. To wait indefinitely, set the value to –1.


### -param completed [out]

Is <b>VARIANT_TRUE</b> if the reports completed; otherwise, <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -remarks



To run the job, call the <a href="https://msdn.microsoft.com/74f369d1-2e3d-49a5-bf54-c1b7c13efbd7">IFsrmReportJob::Run</a> method.

After <b>WaitForCompletion</b> returns, access the <a href="https://msdn.microsoft.com/7a610d10-8e43-49b7-b85b-bb0ec122fda8">IFsrmReportJob::LastError</a> property to determine if the reports completed successfully.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/8087542d-5873-414b-8903-544c2e57cba1">Running a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>



<a href="https://msdn.microsoft.com/74f369d1-2e3d-49a5-bf54-c1b7c13efbd7">IFsrmReportJob::Run</a>
 

 

