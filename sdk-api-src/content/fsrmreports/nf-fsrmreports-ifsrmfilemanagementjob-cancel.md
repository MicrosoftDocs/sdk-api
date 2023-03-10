---
UID: NF:fsrmreports.IFsrmFileManagementJob.Cancel
title: IFsrmFileManagementJob::Cancel (fsrmreports.h)
description: Cancels the job if it is running.
helpviewer_keywords: ["Cancel","Cancel method [File Server Resource Manager]","Cancel method [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","Cancel method","IFsrmFileManagementJob.Cancel","IFsrmFileManagementJob::Cancel","fs.ifsrmfilemanagementjob_cancel","fsrm.ifsrmfilemanagementjob_cancel","fsrmreports/IFsrmFileManagementJob::Cancel"]
old-location: fsrm\ifsrmfilemanagementjob_cancel.htm
tech.root: fsrm
ms.assetid: 3abb6673-fdd8-4828-ba7a-7666208dc8f0
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [File Server Resource Manager], Cancel method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],Cancel method, IFsrmFileManagementJob.Cancel, IFsrmFileManagementJob::Cancel, fs.ifsrmfilemanagementjob_cancel, fsrm.ifsrmfilemanagementjob_cancel, fsrmreports/IFsrmFileManagementJob::Cancel
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
 - IFsrmFileManagementJob::Cancel
 - fsrmreports/IFsrmFileManagementJob::Cancel
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
 - IFsrmFileManagementJob.Cancel
---

# IFsrmFileManagementJob::Cancel


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Cancels the job if it is running.



## -returns

The method returns the following return values.

## -remarks

Cancels the job if the value of its 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_runningstatus">RunningStatus</a> property is 
    <b>FsrmReportRunningStatus_Queued</b> or 
    <b>FsrmReportRunningStatus_Running</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-run">IFsrmFileManagementJob::Run</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
