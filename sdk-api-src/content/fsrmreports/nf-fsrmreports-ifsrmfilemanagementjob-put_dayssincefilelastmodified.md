---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_DaysSinceFileLastModified
title: IFsrmFileManagementJob::put_DaysSinceFileLastModified
author: windows-sdk-content
description: The number of days that have elapsed since a file was last modified.
old-location: fsrm\ifsrmfilemanagementjob_dayssincefilelastmodified.htm
old-project: Fsrm
ms.assetid: 3ee02d60-50c7-4643-9604-b72ca1da01f6
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DaysSinceFileLastModified property [File Server Resource Manager], DaysSinceFileLastModified property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],DaysSinceFileLastModified property, IFsrmFileManagementJob.DaysSinceFileLastModified, IFsrmFileManagementJob.put_DaysSinceFileLastModified, IFsrmFileManagementJob::DaysSinceFileLastModified, IFsrmFileManagementJob::get_DaysSinceFileLastModified, IFsrmFileManagementJob::put_DaysSinceFileLastModified, fs.ifsrmfilemanagementjob_dayssincefilelastmodified, fsrm.ifsrmfilemanagementjob_dayssincefilelastmodified, fsrmreports/IFsrmFileManagementJob::DaysSinceFileLastModified, fsrmreports/IFsrmFileManagementJob::get_DaysSinceFileLastModified, fsrmreports/IFsrmFileManagementJob::put_DaysSinceFileLastModified, put_DaysSinceFileLastModified
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJob.DaysSinceFileLastModified
 - IFsrmFileManagementJob.get_DaysSinceFileLastModified
 - IFsrmFileManagementJob.put_DaysSinceFileLastModified
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::put_DaysSinceFileLastModified


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The number of days that have elapsed since a file was last modified.

This property is read/write.


## -parameters


## -remarks



The value is FsrmDaysNotSpecified if not set.

The job considers this condition met for a file if the file's last modified date minus the job's current run 
    date is less than the value of <i>daysSinceModify</i>.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

