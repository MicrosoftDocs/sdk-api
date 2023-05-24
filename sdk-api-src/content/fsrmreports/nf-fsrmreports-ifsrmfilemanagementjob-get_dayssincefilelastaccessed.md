---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_DaysSinceFileLastAccessed
title: IFsrmFileManagementJob::get_DaysSinceFileLastAccessed (fsrmreports.h)
description: The number of days that have elapsed since the file was last accessed. (Get)
helpviewer_keywords: ["DaysSinceFileLastAccessed property [File Server Resource Manager]","DaysSinceFileLastAccessed property [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","DaysSinceFileLastAccessed property","IFsrmFileManagementJob.DaysSinceFileLastAccessed","IFsrmFileManagementJob.get_DaysSinceFileLastAccessed","IFsrmFileManagementJob::DaysSinceFileLastAccessed","IFsrmFileManagementJob::get_DaysSinceFileLastAccessed","IFsrmFileManagementJob::put_DaysSinceFileLastAccessed","fs.ifsrmfilemanagementjob_dayssincefilelastaccessed","fsrm.ifsrmfilemanagementjob_dayssincefilelastaccessed","fsrmreports/IFsrmFileManagementJob::DaysSinceFileLastAccessed","fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileLastAccessed","fsrmreports/IFsrmFileManagementJob::put_DaysSinceFileLastAccessed","get_DaysSinceFileLastAccessed"]
old-location: fsrm\ifsrmfilemanagementjob_dayssincefilelastaccessed.htm
tech.root: fsrm
ms.assetid: 0892f31d-e2e4-4aeb-9496-f0ff10c2c0af
ms.date: 12/05/2018
ms.keywords: DaysSinceFileLastAccessed property [File Server Resource Manager], DaysSinceFileLastAccessed property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],DaysSinceFileLastAccessed property, IFsrmFileManagementJob.DaysSinceFileLastAccessed, IFsrmFileManagementJob.get_DaysSinceFileLastAccessed, IFsrmFileManagementJob::DaysSinceFileLastAccessed, IFsrmFileManagementJob::get_DaysSinceFileLastAccessed, IFsrmFileManagementJob::put_DaysSinceFileLastAccessed, fs.ifsrmfilemanagementjob_dayssincefilelastaccessed, fsrm.ifsrmfilemanagementjob_dayssincefilelastaccessed, fsrmreports/IFsrmFileManagementJob::DaysSinceFileLastAccessed, fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileLastAccessed, fsrmreports/IFsrmFileManagementJob::put_DaysSinceFileLastAccessed, get_DaysSinceFileLastAccessed
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
 - IFsrmFileManagementJob::get_DaysSinceFileLastAccessed
 - fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileLastAccessed
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
 - IFsrmFileManagementJob.DaysSinceFileLastAccessed
 - IFsrmFileManagementJob.get_DaysSinceFileLastAccessed
 - IFsrmFileManagementJob.put_DaysSinceFileLastAccessed
---

# IFsrmFileManagementJob::get_DaysSinceFileLastAccessed


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The number of days that have elapsed since the file was last accessed.

This property is read/write.

## -parameters

## -remarks

The value is FsrmDaysNotSpecified if not set.

The job considers this condition met for a file if the file's last accessed date minus the job's current run 
    date is less than the value of <i>daysSinceAccess</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
