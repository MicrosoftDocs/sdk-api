---
UID: NF:fsrmreports.IFsrmReportJob.WaitForCompletion
title: IFsrmReportJob::WaitForCompletion (fsrmreports.h)
description: Waits for the reports in the job to complete.
helpviewer_keywords: ["IFsrmReportJob interface [File Server Resource Manager]","WaitForCompletion method","IFsrmReportJob.WaitForCompletion","IFsrmReportJob::WaitForCompletion","WaitForCompletion","WaitForCompletion method [File Server Resource Manager]","WaitForCompletion method [File Server Resource Manager]","IFsrmReportJob interface","fs.ifsrmreportjob_waitforcompletion","fsrm.ifsrmreportjob_waitforcompletion","fsrmreports/IFsrmReportJob::WaitForCompletion"]
old-location: fsrm\ifsrmreportjob_waitforcompletion.htm
tech.root: fsrm
ms.assetid: 127027a0-7f05-4de4-a3be-8e3c3ec30910
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],WaitForCompletion method, IFsrmReportJob.WaitForCompletion, IFsrmReportJob::WaitForCompletion, WaitForCompletion, WaitForCompletion method [File Server Resource Manager], WaitForCompletion method [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_waitforcompletion, fsrm.ifsrmreportjob_waitforcompletion, fsrmreports/IFsrmReportJob::WaitForCompletion
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
 - IFsrmReportJob::WaitForCompletion
 - fsrmreports/IFsrmReportJob::WaitForCompletion
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
 - IFsrmReportJob.WaitForCompletion
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

To run the job, call the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-run">IFsrmReportJob::Run</a> method.

After <b>WaitForCompletion</b> returns, access the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_lasterror">IFsrmReportJob::LastError</a> property to determine if the reports completed successfully.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/running-a-report-job">Running a Report Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-run">IFsrmReportJob::Run</a>