---
UID: NF:fsrmreports.IFsrmReportJob.Run
title: IFsrmReportJob::Run (fsrmreports.h)
description: Runs all the reports in the job.
helpviewer_keywords: ["IFsrmReportJob interface [File Server Resource Manager]","Run method","IFsrmReportJob.Run","IFsrmReportJob::Run","Run","Run method [File Server Resource Manager]","Run method [File Server Resource Manager]","IFsrmReportJob interface","fs.ifsrmreportjob_run","fsrm.ifsrmreportjob_run","fsrmreports/IFsrmReportJob::Run"]
old-location: fsrm\ifsrmreportjob_run.htm
tech.root: fsrm
ms.assetid: 74f369d1-2e3d-49a5-bf54-c1b7c13efbd7
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],Run method, IFsrmReportJob.Run, IFsrmReportJob::Run, Run, Run method [File Server Resource Manager], Run method [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_run, fsrm.ifsrmreportjob_run, fsrmreports/IFsrmReportJob::Run
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportJob::Run
 - fsrmreports/IFsrmReportJob::Run
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
 - IFsrmReportJob.Run
---

# IFsrmReportJob::Run


## -description

Runs all the reports in the job.

## -parameters

### -param context [in]

Specifies to which subdirectory the reports are written. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportgenerationcontext">FsrmReportGenerationContext</a> enumeration.

## -returns

The method returns the following return values.

## -remarks

Note that reports that run in the scheduled context remain in the queue for five minutes before they are run; reports that run in the other contexts remain in the queue for 30 seconds.

If you call this method and the report job is already queued or running, the method returns an error. To determine the status of the job, access the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_runningstatus">IFsrmReportJob::RunningStatus</a> property.


#### Examples

For an example,  see <a href="/previous-versions/windows/desktop/fsrm/running-a-report-job">Running a Report Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-waitforcompletion">IFsrmReportJob::WaitForCompletion</a>