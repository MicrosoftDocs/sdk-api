---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_LastReportPathWithoutExtension
title: IFsrmFileManagementJob::get_LastReportPathWithoutExtension
author: windows-driver-content
description: The local directory path where the reports were stored the last time the job ran.
old-location: fsrm\ifsrmfilemanagementjob_lastreportpathwithoutextension.htm
old-project: Fsrm
ms.assetid: 404d45e0-621e-47d5-b987-0f9347242653
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],LastReportPathWithoutExtension property, IFsrmFileManagementJob.LastReportPathWithoutExtension, IFsrmFileManagementJob.get_LastReportPathWithoutExtension, IFsrmFileManagementJob::LastReportPathWithoutExtension, IFsrmFileManagementJob::get_LastReportPathWithoutExtension, LastReportPathWithoutExtension property [File Server Resource Manager], LastReportPathWithoutExtension property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_lastreportpathwithoutextension, fsrm.ifsrmfilemanagementjob_lastreportpathwithoutextension, fsrmreports/IFsrmFileManagementJob::LastReportPathWithoutExtension, fsrmreports/IFsrmFileManagementJob::get_LastReportPathWithoutExtension, get_LastReportPathWithoutExtension
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileManagementJob.LastReportPathWithoutExtension
-	IFsrmFileManagementJob.get_LastReportPathWithoutExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::get_LastReportPathWithoutExtension


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The local directory path where the reports were stored the last time the job ran.

This property is read-only.


## -parameters


## -remarks



If the job failed, this is the path where the reports would have been stored. The directory may contain 
    reports that completed successfully before the failure occurred.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

