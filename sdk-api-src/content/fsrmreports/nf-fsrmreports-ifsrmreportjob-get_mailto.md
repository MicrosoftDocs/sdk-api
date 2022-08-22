---
UID: NF:fsrmreports.IFsrmReportJob.get_MailTo
title: IFsrmReportJob::get_MailTo (fsrmreports.h)
description: Retrieves or sets the email addresses of those that will receive the reports via email. (Get)
helpviewer_keywords: ["IFsrmReportJob interface [File Server Resource Manager]","MailTo property","IFsrmReportJob.MailTo","IFsrmReportJob.get_MailTo","IFsrmReportJob::MailTo","IFsrmReportJob::get_MailTo","IFsrmReportJob::put_MailTo","MailTo property [File Server Resource Manager]","MailTo property [File Server Resource Manager]","IFsrmReportJob interface","fs.ifsrmreportjob_mailto","fsrm.ifsrmreportjob_mailto","fsrmreports/IFsrmReportJob::MailTo","fsrmreports/IFsrmReportJob::get_MailTo","fsrmreports/IFsrmReportJob::put_MailTo","get_MailTo"]
old-location: fsrm\ifsrmreportjob_mailto.htm
tech.root: fsrm
ms.assetid: 8ec5d65a-9729-4d68-bceb-b07a2f56755e
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],MailTo property, IFsrmReportJob.MailTo, IFsrmReportJob.get_MailTo, IFsrmReportJob::MailTo, IFsrmReportJob::get_MailTo, IFsrmReportJob::put_MailTo, MailTo property [File Server Resource Manager], MailTo property [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_mailto, fsrm.ifsrmreportjob_mailto, fsrmreports/IFsrmReportJob::MailTo, fsrmreports/IFsrmReportJob::get_MailTo, fsrmreports/IFsrmReportJob::put_MailTo, get_MailTo
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
 - IFsrmReportJob::get_MailTo
 - fsrmreports/IFsrmReportJob::get_MailTo
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
 - IFsrmReportJob.MailTo
 - IFsrmReportJob.get_MailTo
 - IFsrmReportJob.put_MailTo
---

# IFsrmReportJob::get_MailTo


## -description

Retrieves or sets the email addresses of those that will receive the reports via email.

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

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>
