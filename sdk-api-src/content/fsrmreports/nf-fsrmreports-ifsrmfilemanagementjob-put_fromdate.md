---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_FromDate
title: IFsrmFileManagementJob::put_FromDate method
author: windows-driver-content
description: The date from which you want the file management job to begin expiring files (moving files to the expired files directory). This property also applies to custom commands for the file management job.
old-location: fsrm\ifsrmfilemanagementjob_fromdate.htm
old-project: Fsrm
ms.assetid: f891679d-3d94-4fbe-99b1-9445666b7694
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: FromDate property [File Server Resource Manager], FromDate property [File Server Resource Manager], IFsrmFileManagementJob interface, IFsrmFileManagementJob, IFsrmFileManagementJob interface [File Server Resource Manager], FromDate property, IFsrmFileManagementJob.FromDate, IFsrmFileManagementJob::get_FromDate, IFsrmFileManagementJob::put_FromDate, fs.ifsrmfilemanagementjob_fromdate, fsrm.ifsrmfilemanagementjob_fromdate, fsrmreports/IFsrmFileManagementJob::FromDate, fsrmreports/IFsrmFileManagementJob::get_FromDate, fsrmreports/IFsrmFileManagementJob::put_FromDate, put_FromDate,IFsrmFileManagementJob.put_FromDate
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileManagementJob.FromDate
-	IFsrmFileManagementJob.get_FromDate
-	IFsrmFileManagementJob.put_FromDate
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::put_FromDate method


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The date from which you want the file management job to begin expiring files (moving files to the 
    expired files directory). This property also applies to custom commands for the file management job.

This property is read/write.


## -parameters


## -remarks



The value is FsrmDateNotSpecified if not set.

The job expires the files if the <i>fromDate</i> value is earlier than the job's current 
    run date.

Typically, you set this date to be greater than the shortest notification period that you specify. This 
    ensures that notification is sent at least once before files are expired. If you do not specify this date, files 
    can be expired before notification is sent. For example, if you create job and run it the same day, it is possible 
    that one or more files will meet the expiration conditions set by the job and be expired without any notification. 
    You can create zero-day notification but the notification will be after the fact.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

