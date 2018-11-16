---
UID: NF:fsrmreports.IFsrmFileManagementJob.WaitForCompletion
title: IFsrmFileManagementJob::WaitForCompletion
author: windows-sdk-content
description: Waits for the specified period of time or until the job has finished running.
old-location: fsrm\ifsrmfilemanagementjob_waitforcompletion.htm
tech.root: Fsrm
ms.assetid: 8d0d0046-989f-4d6a-b9da-caf6df44e1db
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],WaitForCompletion method, IFsrmFileManagementJob.WaitForCompletion, IFsrmFileManagementJob::WaitForCompletion, WaitForCompletion, WaitForCompletion method [File Server Resource Manager], WaitForCompletion method [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_waitforcompletion, fsrm.ifsrmfilemanagementjob_waitforcompletion, fsrmreports/IFsrmFileManagementJob::WaitForCompletion
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJob.WaitForCompletion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmreports.h
: 
- IFsrmFileManagementJob.WaitForCompletion
: 
---

# IFsrmFileManagementJob::WaitForCompletion


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

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
    <a href="https://msdn.microsoft.com/2db27e05-5c3b-4827-a616-36fd46281911">IFsrmFileManagementJob::Run</a> method. Jobs run 
     asynchronously, calling this method blocks your thread until the job completes or the timeout period 
     expires.

After <b>WaitForCompletion</b> 
     returns, access the 
     <a href="https://msdn.microsoft.com/f7a7d5fd-b060-41f6-be1f-038ab252259a">IFsrmFileManagementJob::LastError</a> 
     property to determine if the reports completed successfully.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

