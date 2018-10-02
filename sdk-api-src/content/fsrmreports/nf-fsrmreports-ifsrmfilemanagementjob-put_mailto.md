---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_MailTo
title: IFsrmFileManagementJob::put_MailTo
author: windows-sdk-content
description: The email addresses to which to send the reports, if any.
old-location: fsrm\ifsrmfilemanagementjob_mailto.htm
tech.root: Fsrm
ms.assetid: 5a6fdb6f-ac95-448c-bbf4-cbcbaf942bd4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],MailTo property, IFsrmFileManagementJob.MailTo, IFsrmFileManagementJob.put_MailTo, IFsrmFileManagementJob::MailTo, IFsrmFileManagementJob::get_MailTo, IFsrmFileManagementJob::put_MailTo, MailTo property [File Server Resource Manager], MailTo property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_mailto, fsrm.ifsrmfilemanagementjob_mailto, fsrmreports/IFsrmFileManagementJob::MailTo, fsrmreports/IFsrmFileManagementJob::get_MailTo, fsrmreports/IFsrmFileManagementJob::put_MailTo, put_MailTo
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
 - IFsrmFileManagementJob.MailTo
 - IFsrmFileManagementJob.get_MailTo
 - IFsrmFileManagementJob.put_MailTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::put_MailTo


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The email addresses to which to send the reports, if any.

This property is read/write.


## -parameters


## -remarks



This property is optional.

The email message is sent only if the job finishes successfully. Email is not sent for 
    <b>FsrmReportType_ExportReport</b> report types. The reports are attached to the email 
    message. You can specify [Admin Email] to send notification to the administrator (if the 
    <a href="https://msdn.microsoft.com/5985f697-f982-481c-896e-e6c3834f645d">IFsrmSetting::AdminEmail</a> property is set). The 
    subject is "&lt;ReportType&gt;: &lt;ReportName&gt;". The body of the email message is empty.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

