---
UID: NF:fsrm.IFsrmActionEmail.get_MailReplyTo
title: IFsrmActionEmail::get_MailReplyTo
author: windows-sdk-content
description: Retrieves or sets the email address to use as the reply-to address when the recipient of the email message replies.
old-location: fsrm\ifsrmactionemail_mailreplyto.htm
old-project: Fsrm
ms.assetid: 54d1b801-1df5-4712-9b2e-6a993a62b48a
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmActionEmail interface [File Server Resource Manager],MailReplyTo property, IFsrmActionEmail.MailReplyTo, IFsrmActionEmail.get_MailReplyTo, IFsrmActionEmail2 interface [File Server Resource Manager],MailReplyTo property, IFsrmActionEmail2.MailReplyTo, IFsrmActionEmail2::MailReplyTo, IFsrmActionEmail2::get_MailReplyTo, IFsrmActionEmail2::put_MailReplyTo, IFsrmActionEmail::get_MailReplyTo, IFsrmActionEmail::put_MailReplyTo, MailReplyTo property [File Server Resource Manager], MailReplyTo property [File Server Resource Manager],IFsrmActionEmail interface, MailReplyTo property [File Server Resource Manager],IFsrmActionEmail2 interface, fs.ifsrmactionemail_mailreplyto, fsrm.ifsrmactionemail_mailreplyto, fsrm/IFsrmActionEmail2::MailReplyTo, fsrm/IFsrmActionEmail2::get_MailReplyTo, fsrm/IFsrmActionEmail2::put_MailReplyTo, fsrm/IFsrmActionEmail::MailReplyTo, fsrm/IFsrmActionEmail::get_MailReplyTo, fsrm/IFsrmActionEmail::put_MailReplyTo, get_MailReplyTo
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmActionEmail2.MailReplyTo
-	IFsrmActionEmail2.get_MailReplyTo
-	IFsrmActionEmail2.put_MailReplyTo
-	IFsrmActionEmail.MailReplyTo
-	IFsrmActionEmail.get_MailReplyTo
-	IFsrmActionEmail.put_MailReplyTo
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmActionEmail::get_MailReplyTo


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the email address to use as the reply-to address when the recipient of the email 
    message replies.

This property is read/write.


## -parameters


## -remarks



If the user specified  in the <a href="https://msdn.microsoft.com/b440bae5-0e46-432b-992b-0de7dee16b12">MailTo</a> 
    property replies to the email message (for example, the user wants to request a quota increase), the reply is sent 
    to the user specified in the <b>MailReplyTo</b> 
    property. If <b>MailReplyTo</b> is not set, the 
    reply is sent to the user specified in the 
    <a href="https://msdn.microsoft.com/67fb5ae6-7728-4c95-92d6-f36859346cc7">MailFrom</a> property.




## -see-also




<a href="https://msdn.microsoft.com/6eb6d82e-018d-4977-ad60-fce296c16e83">IFsrmActionEmail</a>



<a href="https://msdn.microsoft.com/278ef98d-fb1d-42a4-a740-07c5e713a230">IFsrmActionEmail2</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

