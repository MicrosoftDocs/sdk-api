---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_ReportEnabled
title: IFsrmFileManagementJob::put_ReportEnabled (fsrmreports.h)
description: Indicates whether the job will generate a report when it runs. (Put)
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","ReportEnabled property","IFsrmFileManagementJob.ReportEnabled","IFsrmFileManagementJob.put_ReportEnabled","IFsrmFileManagementJob::ReportEnabled","IFsrmFileManagementJob::get_ReportEnabled","IFsrmFileManagementJob::put_ReportEnabled","ReportEnabled property [File Server Resource Manager]","ReportEnabled property [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_reportenabled","fsrm.ifsrmfilemanagementjob_reportenabled","fsrmreports/IFsrmFileManagementJob::ReportEnabled","fsrmreports/IFsrmFileManagementJob::get_ReportEnabled","fsrmreports/IFsrmFileManagementJob::put_ReportEnabled","put_ReportEnabled"]
old-location: fsrm\ifsrmfilemanagementjob_reportenabled.htm
tech.root: fsrm
ms.assetid: 687367c7-5bed-4f42-ade1-f841da484b38
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],ReportEnabled property, IFsrmFileManagementJob.ReportEnabled, IFsrmFileManagementJob.put_ReportEnabled, IFsrmFileManagementJob::ReportEnabled, IFsrmFileManagementJob::get_ReportEnabled, IFsrmFileManagementJob::put_ReportEnabled, ReportEnabled property [File Server Resource Manager], ReportEnabled property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_reportenabled, fsrm.ifsrmfilemanagementjob_reportenabled, fsrmreports/IFsrmFileManagementJob::ReportEnabled, fsrmreports/IFsrmFileManagementJob::get_ReportEnabled, fsrmreports/IFsrmFileManagementJob::put_ReportEnabled, put_ReportEnabled
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
 - IFsrmFileManagementJob::put_ReportEnabled
 - fsrmreports/IFsrmFileManagementJob::put_ReportEnabled
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
 - IFsrmFileManagementJob.ReportEnabled
 - IFsrmFileManagementJob.get_ReportEnabled
 - IFsrmFileManagementJob.put_ReportEnabled
---

# IFsrmFileManagementJob::put_ReportEnabled


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Indicates whether the job will generate a report when it runs.

This property is read/write.

## -parameters

## -remarks

The job generates a default report that it places in the folder associated with context specified when you run 
    the job.

Controls reporting regardless of whether the file management job was scheduled (using the Task Scheduler) or 
    run on demand (using 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-run">IFsrmFileManagementJob::Run</a>).

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
