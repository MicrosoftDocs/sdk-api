---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_ReportEnabled
title: IFsrmFileManagementJob::get_ReportEnabled
author: windows-sdk-content
description: Indicates whether the job will generate a report when it runs.
old-location: fsrm\ifsrmfilemanagementjob_reportenabled.htm
tech.root: Fsrm
ms.assetid: 687367c7-5bed-4f42-ade1-f841da484b38
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],ReportEnabled property, IFsrmFileManagementJob.ReportEnabled, IFsrmFileManagementJob.get_ReportEnabled, IFsrmFileManagementJob::ReportEnabled, IFsrmFileManagementJob::get_ReportEnabled, IFsrmFileManagementJob::put_ReportEnabled, ReportEnabled property [File Server Resource Manager], ReportEnabled property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_reportenabled, fsrm.ifsrmfilemanagementjob_reportenabled, fsrmreports/IFsrmFileManagementJob::ReportEnabled, fsrmreports/IFsrmFileManagementJob::get_ReportEnabled, fsrmreports/IFsrmFileManagementJob::put_ReportEnabled, get_ReportEnabled
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
 - IFsrmFileManagementJob.ReportEnabled
 - IFsrmFileManagementJob.get_ReportEnabled
 - IFsrmFileManagementJob.put_ReportEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmreports.h
: 
- IFsrmFileManagementJob.get_ReportEnabled
: 
---

# IFsrmFileManagementJob::get_ReportEnabled


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Indicates whether the job will generate a report when it runs.

This property is read/write.


## -parameters


## -remarks



The job generates a default report that it places in the folder associated with context specified when you run 
    the job.

Controls reporting regardless of whether the file management job was scheduled (using the Task Scheduler) or 
    run on demand (using 
    <a href="https://msdn.microsoft.com/2db27e05-5c3b-4827-a616-36fd46281911">IFsrmFileManagementJob::Run</a>).




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

