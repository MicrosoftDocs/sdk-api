---
UID: NF:fsrmreports.IFsrmFileManagementJob.Run
title: IFsrmFileManagementJob::Run (fsrmreports.h)
description: Runs the job.
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","Run method","IFsrmFileManagementJob.Run","IFsrmFileManagementJob::Run","Run","Run method [File Server Resource Manager]","Run method [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_run","fsrm.ifsrmfilemanagementjob_run","fsrmreports/IFsrmFileManagementJob::Run"]
old-location: fsrm\ifsrmfilemanagementjob_run.htm
tech.root: fsrm
ms.assetid: 2db27e05-5c3b-4827-a616-36fd46281911
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],Run method, IFsrmFileManagementJob.Run, IFsrmFileManagementJob::Run, Run, Run method [File Server Resource Manager], Run method [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_run, fsrm.ifsrmfilemanagementjob_run, fsrmreports/IFsrmFileManagementJob::Run
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
 - IFsrmFileManagementJob::Run
 - fsrmreports/IFsrmFileManagementJob::Run
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
 - IFsrmFileManagementJob.Run
---

# IFsrmFileManagementJob::Run


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Runs the job.

## -parameters

### -param context [in]

Specifies to which subdirectory the reports or logging are written, if enabled. For possible values, see 
      the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportgenerationcontext">FsrmReportGenerationContext</a> 
      enumeration.

## -returns

The method returns the following return values.

## -remarks

Since the file management job consumes the results of classification, running the file management job also 
    runs classification.

The jobs are run asynchronously. Jobs that run in the scheduled context remain in the queue for five minutes 
    before they are run; jobs that run in the other contexts remain in the queue for 30 seconds. To block your code 
    until the job completes, calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-waitforcompletion">IFsrmFileManagementJob::WaitForCompletion</a> 
    method. Calling <b>WaitForCompletion</b> 
    removes the job from the queue and runs it immediately.

If you call this method and the job is already queued or running, the method returns an error. To determine 
    the status of the job, access the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_runningstatus">IFsrmReportJob::RunningStatus</a> 
    property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>