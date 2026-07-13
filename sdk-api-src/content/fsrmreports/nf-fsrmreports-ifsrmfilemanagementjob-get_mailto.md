---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_MailTo
title: IFsrmFileManagementJob::get_MailTo (fsrmreports.h)
description: The email addresses to which to send the reports, if any. (Get)
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","MailTo property","IFsrmFileManagementJob.MailTo","IFsrmFileManagementJob.get_MailTo","IFsrmFileManagementJob::MailTo","IFsrmFileManagementJob::get_MailTo","IFsrmFileManagementJob::put_MailTo","MailTo property [File Server Resource Manager]","MailTo property [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_mailto","fsrm.ifsrmfilemanagementjob_mailto","fsrmreports/IFsrmFileManagementJob::MailTo","fsrmreports/IFsrmFileManagementJob::get_MailTo","fsrmreports/IFsrmFileManagementJob::put_MailTo","get_MailTo"]
old-location: fsrm\ifsrmfilemanagementjob_mailto.htm
tech.root: fsrm
ms.assetid: 5a6fdb6f-ac95-448c-bbf4-cbcbaf942bd4
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],MailTo property, IFsrmFileManagementJob.MailTo, IFsrmFileManagementJob.get_MailTo, IFsrmFileManagementJob::MailTo, IFsrmFileManagementJob::get_MailTo, IFsrmFileManagementJob::put_MailTo, MailTo property [File Server Resource Manager], MailTo property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_mailto, fsrm.ifsrmfilemanagementjob_mailto, fsrmreports/IFsrmFileManagementJob::MailTo, fsrmreports/IFsrmFileManagementJob::get_MailTo, fsrmreports/IFsrmFileManagementJob::put_MailTo, get_MailTo
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
 - IFsrmFileManagementJob::get_MailTo
 - fsrmreports/IFsrmFileManagementJob::get_MailTo
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
 - IFsrmFileManagementJob.MailTo
 - IFsrmFileManagementJob.get_MailTo
 - IFsrmFileManagementJob.put_MailTo
---

# IFsrmFileManagementJob::get_MailTo


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The email addresses to which to send the reports, if any.

This property is read/write.

## -parameters

## -remarks

This property is optional.

The email message is sent only if the job finishes successfully. Email is not sent for 
    <b>FsrmReportType_ExportReport</b> report types. The reports are attached to the email 
    message. You can specify [Admin Email] to send notification to the administrator (if the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_adminemail">IFsrmSetting::AdminEmail</a> property is set). The 
    subject is "&lt;ReportType&gt;: &lt;ReportName&gt;". The body of the email message is empty.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
