---
UID: NF:fsrm.IFsrmActionReport.get_MailTo
title: IFsrmActionReport::get_MailTo (fsrm.h)
description: Retrieves or sets the email address to which the reports are sent. (Get)
helpviewer_keywords: ["IFsrmActionReport interface [File Server Resource Manager]","MailTo property","IFsrmActionReport.MailTo","IFsrmActionReport.get_MailTo","IFsrmActionReport::MailTo","IFsrmActionReport::get_MailTo","IFsrmActionReport::put_MailTo","MailTo property [File Server Resource Manager]","MailTo property [File Server Resource Manager]","IFsrmActionReport interface","fs.ifsrmactionreport_mailto","fsrm.ifsrmactionreport_mailto","fsrm/IFsrmActionReport::MailTo","fsrm/IFsrmActionReport::get_MailTo","fsrm/IFsrmActionReport::put_MailTo","get_MailTo"]
old-location: fsrm\ifsrmactionreport_mailto.htm
tech.root: fsrm
ms.assetid: 89c2fc2c-bf14-4a42-b7ab-12988433b275
ms.date: 12/05/2018
ms.keywords: IFsrmActionReport interface [File Server Resource Manager],MailTo property, IFsrmActionReport.MailTo, IFsrmActionReport.get_MailTo, IFsrmActionReport::MailTo, IFsrmActionReport::get_MailTo, IFsrmActionReport::put_MailTo, MailTo property [File Server Resource Manager], MailTo property [File Server Resource Manager],IFsrmActionReport interface, fs.ifsrmactionreport_mailto, fsrm.ifsrmactionreport_mailto, fsrm/IFsrmActionReport::MailTo, fsrm/IFsrmActionReport::get_MailTo, fsrm/IFsrmActionReport::put_MailTo, get_MailTo
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmScreen.h
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
 - IFsrmActionReport::get_MailTo
 - fsrm/IFsrmActionReport::get_MailTo
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
 - IFsrmActionReport.MailTo
 - IFsrmActionReport.get_MailTo
 - IFsrmActionReport.put_MailTo
---

# IFsrmActionReport::get_MailTo


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the email address to which the reports are sent.

This property is read/write.

## -parameters

## -remarks

The email message contains the reports as attachments. It is possible that the mail server may reject the 
    message if the server limits attachment sizes. The 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_mailfrom">IFsrmSetting::MailFrom</a> property specifies the 
    sender of the email. The subject and message body contain predefined text that identifies the quota that caused 
    the notification. The email addresses are not checked for format until the action is run.

You can also call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">IFsrmReportManager::SetOutputDirectory</a> 
    method to specify the storage location for these incident reports.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/updating-a-quota">Updating a Quota</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionreport">IFsrmActionReport</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
