---
UID: NF:fsrmreports.IFsrmFileManagementJob.WaitForCompletion
title: IFsrmFileManagementJob::WaitForCompletion (fsrmreports.h)
description: Waits for the specified period of time or until the job has finished running.
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","WaitForCompletion method","IFsrmFileManagementJob.WaitForCompletion","IFsrmFileManagementJob::WaitForCompletion","WaitForCompletion","WaitForCompletion method [File Server Resource Manager]","WaitForCompletion method [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_waitforcompletion","fsrm.ifsrmfilemanagementjob_waitforcompletion","fsrmreports/IFsrmFileManagementJob::WaitForCompletion"]
old-location: fsrm\ifsrmfilemanagementjob_waitforcompletion.htm
tech.root: fsrm
ms.assetid: 8d0d0046-989f-4d6a-b9da-caf6df44e1db
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],WaitForCompletion method, IFsrmFileManagementJob.WaitForCompletion, IFsrmFileManagementJob::WaitForCompletion, WaitForCompletion, WaitForCompletion method [File Server Resource Manager], WaitForCompletion method [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_waitforcompletion, fsrm.ifsrmfilemanagementjob_waitforcompletion, fsrmreports/IFsrmFileManagementJob::WaitForCompletion
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
 - IFsrmFileManagementJob::WaitForCompletion
 - fsrmreports/IFsrmFileManagementJob::WaitForCompletion
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
 - IFsrmFileManagementJob.WaitForCompletion
---

# IFsrmFileManagementJob::WaitForCompletion


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Waits for the specified period of time or until the job has finished running.

## -parameters

### -param waitSeconds [in]

The number of seconds to wait for the job to complete. The method returns when the period expires or the 
      job complete. To wait indefinitely, set the value to –1.

### -param completed [out]

Is <b>VARIANT_TRUE</b> if the job completed; otherwise, 
      <b>VARIANT_FALSE</b>.

## -returns

The method returns the following return values.

## -remarks

To run the job, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-run">IFsrmFileManagementJob::Run</a> method. Jobs run 
     asynchronously, calling this method blocks your thread until the job completes or the timeout period 
     expires.

After <b>WaitForCompletion</b> 
     returns, access the 
     <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_lasterror">IFsrmFileManagementJob::LastError</a> 
     property to determine if the reports completed successfully.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>