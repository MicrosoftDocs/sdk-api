---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_DaysSinceFileCreated
title: IFsrmFileManagementJob::put_DaysSinceFileCreated
author: windows-sdk-content
description: The number of days that have elapsed since the file was created.
old-location: fsrm\ifsrmfilemanagementjob_dayssincefilecreated.htm
tech.root: Fsrm
ms.assetid: f897321f-3e32-4965-b6c0-33d156601481
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DaysSinceFileCreated property [File Server Resource Manager], DaysSinceFileCreated property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],DaysSinceFileCreated property, IFsrmFileManagementJob.DaysSinceFileCreated, IFsrmFileManagementJob.put_DaysSinceFileCreated, IFsrmFileManagementJob::DaysSinceFileCreated, IFsrmFileManagementJob::get_DaysSinceFileCreated, IFsrmFileManagementJob::put_DaysSinceFileCreated, fs.ifsrmfilemanagementjob_dayssincefilecreated, fsrm.ifsrmfilemanagementjob_dayssincefilecreated, fsrmreports/IFsrmFileManagementJob::DaysSinceFileCreated, fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileCreated, fsrmreports/IFsrmFileManagementJob::put_DaysSinceFileCreated, put_DaysSinceFileCreated
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
 - IFsrmFileManagementJob.DaysSinceFileCreated
 - IFsrmFileManagementJob.get_DaysSinceFileCreated
 - IFsrmFileManagementJob.put_DaysSinceFileCreated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::put_DaysSinceFileCreated


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The number of days that have elapsed since the file was created.

This property is read/write.


## -parameters


## -remarks



The value is FsrmDaysNotSpecified if not set.

The job considers this condition met for a file if the file's creation date minus the job's current run date 
    is less than the value of <i>daysSinceCreation</i>.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

