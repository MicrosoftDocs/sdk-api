---
UID: NF:fsrm.IFsrmActionReport.get_MailTo
title: IFsrmActionReport::get_MailTo
author: windows-sdk-content
description: Retrieves or sets the email address to which the reports are sent.
old-location: fsrm\ifsrmactionreport_mailto.htm
old-project: fsrm
ms.assetid: 89c2fc2c-bf14-4a42-b7ab-12988433b275
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IFsrmActionReport interface [File Server Resource Manager],MailTo property, IFsrmActionReport.MailTo, IFsrmActionReport.get_MailTo, IFsrmActionReport::MailTo, IFsrmActionReport::get_MailTo, IFsrmActionReport::put_MailTo, MailTo property [File Server Resource Manager], MailTo property [File Server Resource Manager],IFsrmActionReport interface, fs.ifsrmactionreport_mailto, fsrm.ifsrmactionreport_mailto, fsrm/IFsrmActionReport::MailTo, fsrm/IFsrmActionReport::get_MailTo, fsrm/IFsrmActionReport::put_MailTo, get_MailTo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmActionReport::get_MailTo


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the email address to which the reports are sent.

This property is read/write.


## -parameters


## -remarks



The email message contains the reports as attachments. It is possible that the mail server may reject the 
    message if the server limits attachment sizes. The 
    <a href="https://msdn.microsoft.com/62296c6c-d75b-4669-a665-a0c4321218b6">IFsrmSetting::MailFrom</a> property specifies the 
    sender of the email. The subject and message body contain predefined text that identifies the quota that caused 
    the notification. The email addresses are not checked for format until the action is run.

You can also call the 
    <a href="https://msdn.microsoft.com/5bbc4255-1fed-45c5-bb13-41ee7c47ed56">IFsrmReportManager::SetOutputDirectory</a> 
    method to specify the storage location for these incident reports.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/fce6ce55-3fb5-46bc-8f26-3071df54767e">Updating a Quota</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/efff4cec-6985-40aa-a74e-bb2afdeb2a0a">IFsrmActionReport</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

