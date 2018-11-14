---
UID: NF:fsrmreports.IFsrmFileManagementJob.Cancel
title: IFsrmFileManagementJob::Cancel
author: windows-sdk-content
description: Cancels the job if it is running.
old-location: fsrm\ifsrmfilemanagementjob_cancel.htm
tech.root: Fsrm
ms.assetid: 3abb6673-fdd8-4828-ba7a-7666208dc8f0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Cancel, Cancel method [File Server Resource Manager], Cancel method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],Cancel method, IFsrmFileManagementJob.Cancel, IFsrmFileManagementJob::Cancel, fs.ifsrmfilemanagementjob_cancel, fsrm.ifsrmfilemanagementjob_cancel, fsrmreports/IFsrmFileManagementJob::Cancel
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
 - IFsrmFileManagementJob.Cancel
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
- IFsrmFileManagementJob.Cancel
: 
---

# IFsrmFileManagementJob::Cancel


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Cancels the job if it is running.


## -parameters






## -returns



The method returns the following return values.




## -remarks



Cancels the job if the value of its 
    <a href="https://msdn.microsoft.com/030efc19-69c0-4321-99ac-ff8abfc38757">RunningStatus</a> property is 
    <b>FsrmReportRunningStatus_Queued</b> or 
    <b>FsrmReportRunningStatus_Running</b>.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/2db27e05-5c3b-4827-a616-36fd46281911">IFsrmFileManagementJob::Run</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

