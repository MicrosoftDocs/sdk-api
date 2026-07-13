---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_DaysSinceFileCreated
title: IFsrmFileManagementJob::get_DaysSinceFileCreated (fsrmreports.h)
description: The number of days that have elapsed since the file was created. (Get)
helpviewer_keywords: ["DaysSinceFileCreated property [File Server Resource Manager]","DaysSinceFileCreated property [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","DaysSinceFileCreated property","IFsrmFileManagementJob.DaysSinceFileCreated","IFsrmFileManagementJob.get_DaysSinceFileCreated","IFsrmFileManagementJob::DaysSinceFileCreated","IFsrmFileManagementJob::get_DaysSinceFileCreated","IFsrmFileManagementJob::put_DaysSinceFileCreated","fs.ifsrmfilemanagementjob_dayssincefilecreated","fsrm.ifsrmfilemanagementjob_dayssincefilecreated","fsrmreports/IFsrmFileManagementJob::DaysSinceFileCreated","fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileCreated","fsrmreports/IFsrmFileManagementJob::put_DaysSinceFileCreated","get_DaysSinceFileCreated"]
old-location: fsrm\ifsrmfilemanagementjob_dayssincefilecreated.htm
tech.root: fsrm
ms.assetid: f897321f-3e32-4965-b6c0-33d156601481
ms.date: 12/05/2018
ms.keywords: DaysSinceFileCreated property [File Server Resource Manager], DaysSinceFileCreated property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],DaysSinceFileCreated property, IFsrmFileManagementJob.DaysSinceFileCreated, IFsrmFileManagementJob.get_DaysSinceFileCreated, IFsrmFileManagementJob::DaysSinceFileCreated, IFsrmFileManagementJob::get_DaysSinceFileCreated, IFsrmFileManagementJob::put_DaysSinceFileCreated, fs.ifsrmfilemanagementjob_dayssincefilecreated, fsrm.ifsrmfilemanagementjob_dayssincefilecreated, fsrmreports/IFsrmFileManagementJob::DaysSinceFileCreated, fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileCreated, fsrmreports/IFsrmFileManagementJob::put_DaysSinceFileCreated, get_DaysSinceFileCreated
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
 - IFsrmFileManagementJob::get_DaysSinceFileCreated
 - fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileCreated
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
 - IFsrmFileManagementJob.DaysSinceFileCreated
 - IFsrmFileManagementJob.get_DaysSinceFileCreated
 - IFsrmFileManagementJob.put_DaysSinceFileCreated
---

# IFsrmFileManagementJob::get_DaysSinceFileCreated


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The number of days that have elapsed since the file was created.

This property is read/write.

## -parameters

## -remarks

The value is FsrmDaysNotSpecified if not set.

The job considers this condition met for a file if the file's creation date minus the job's current run date 
    is less than the value of <i>daysSinceCreation</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
