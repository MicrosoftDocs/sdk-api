---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_FromDate
title: IFsrmFileManagementJob::put_FromDate (fsrmreports.h)
description: The date from which you want the file management job to begin expiring files (moving files to the expired files directory). This property also applies to custom commands for the file management job. (Put)
helpviewer_keywords: ["FromDate property [File Server Resource Manager]","FromDate property [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","FromDate property","IFsrmFileManagementJob.FromDate","IFsrmFileManagementJob.put_FromDate","IFsrmFileManagementJob::FromDate","IFsrmFileManagementJob::get_FromDate","IFsrmFileManagementJob::put_FromDate","fs.ifsrmfilemanagementjob_fromdate","fsrm.ifsrmfilemanagementjob_fromdate","fsrmreports/IFsrmFileManagementJob::FromDate","fsrmreports/IFsrmFileManagementJob::get_FromDate","fsrmreports/IFsrmFileManagementJob::put_FromDate","put_FromDate"]
old-location: fsrm\ifsrmfilemanagementjob_fromdate.htm
tech.root: fsrm
ms.assetid: f891679d-3d94-4fbe-99b1-9445666b7694
ms.date: 12/05/2018
ms.keywords: FromDate property [File Server Resource Manager], FromDate property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],FromDate property, IFsrmFileManagementJob.FromDate, IFsrmFileManagementJob.put_FromDate, IFsrmFileManagementJob::FromDate, IFsrmFileManagementJob::get_FromDate, IFsrmFileManagementJob::put_FromDate, fs.ifsrmfilemanagementjob_fromdate, fsrm.ifsrmfilemanagementjob_fromdate, fsrmreports/IFsrmFileManagementJob::FromDate, fsrmreports/IFsrmFileManagementJob::get_FromDate, fsrmreports/IFsrmFileManagementJob::put_FromDate, put_FromDate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmFileManagementJob::put_FromDate
 - fsrmreports/IFsrmFileManagementJob::put_FromDate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJob.FromDate
 - IFsrmFileManagementJob.get_FromDate
 - IFsrmFileManagementJob.put_FromDate
---

# IFsrmFileManagementJob::put_FromDate


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

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

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
