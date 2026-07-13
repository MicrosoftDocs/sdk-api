---
UID: NF:fsrm.IFsrmActionEmail.get_MailReplyTo
title: IFsrmActionEmail::get_MailReplyTo (fsrm.h)
description: Retrieves or sets the email address to use as the reply-to address when the recipient of the email message replies. (Get)
helpviewer_keywords: ["IFsrmActionEmail interface [File Server Resource Manager]","MailReplyTo property","IFsrmActionEmail.MailReplyTo","IFsrmActionEmail.get_MailReplyTo","IFsrmActionEmail2 interface [File Server Resource Manager]","MailReplyTo property","IFsrmActionEmail2.MailReplyTo","IFsrmActionEmail2::MailReplyTo","IFsrmActionEmail2::get_MailReplyTo","IFsrmActionEmail2::put_MailReplyTo","IFsrmActionEmail::get_MailReplyTo","IFsrmActionEmail::put_MailReplyTo","MailReplyTo property [File Server Resource Manager]","MailReplyTo property [File Server Resource Manager]","IFsrmActionEmail interface","MailReplyTo property [File Server Resource Manager]","IFsrmActionEmail2 interface","fs.ifsrmactionemail_mailreplyto","fsrm.ifsrmactionemail_mailreplyto","fsrm/IFsrmActionEmail2::MailReplyTo","fsrm/IFsrmActionEmail2::get_MailReplyTo","fsrm/IFsrmActionEmail2::put_MailReplyTo","fsrm/IFsrmActionEmail::MailReplyTo","fsrm/IFsrmActionEmail::get_MailReplyTo","fsrm/IFsrmActionEmail::put_MailReplyTo","get_MailReplyTo"]
old-location: fsrm\ifsrmactionemail_mailreplyto.htm
tech.root: fsrm
ms.assetid: 54d1b801-1df5-4712-9b2e-6a993a62b48a
ms.date: 12/05/2018
ms.keywords: IFsrmActionEmail interface [File Server Resource Manager],MailReplyTo property, IFsrmActionEmail.MailReplyTo, IFsrmActionEmail.get_MailReplyTo, IFsrmActionEmail2 interface [File Server Resource Manager],MailReplyTo property, IFsrmActionEmail2.MailReplyTo, IFsrmActionEmail2::MailReplyTo, IFsrmActionEmail2::get_MailReplyTo, IFsrmActionEmail2::put_MailReplyTo, IFsrmActionEmail::get_MailReplyTo, IFsrmActionEmail::put_MailReplyTo, MailReplyTo property [File Server Resource Manager], MailReplyTo property [File Server Resource Manager],IFsrmActionEmail interface, MailReplyTo property [File Server Resource Manager],IFsrmActionEmail2 interface, fs.ifsrmactionemail_mailreplyto, fsrm.ifsrmactionemail_mailreplyto, fsrm/IFsrmActionEmail2::MailReplyTo, fsrm/IFsrmActionEmail2::get_MailReplyTo, fsrm/IFsrmActionEmail2::put_MailReplyTo, fsrm/IFsrmActionEmail::MailReplyTo, fsrm/IFsrmActionEmail::get_MailReplyTo, fsrm/IFsrmActionEmail::put_MailReplyTo, get_MailReplyTo
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
 - IFsrmActionEmail::get_MailReplyTo
 - fsrm/IFsrmActionEmail::get_MailReplyTo
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
 - IFsrmActionEmail2.MailReplyTo
 - IFsrmActionEmail2.get_MailReplyTo
 - IFsrmActionEmail2.put_MailReplyTo
 - IFsrmActionEmail.MailReplyTo
 - IFsrmActionEmail.get_MailReplyTo
 - IFsrmActionEmail.put_MailReplyTo
---

# IFsrmActionEmail::get_MailReplyTo


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the email address to use as the reply-to address when the recipient of the email 
    message replies.

This property is read/write.

## -parameters

## -remarks

If the user specified  in the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactionemail-get_mailto">MailTo</a> 
    property replies to the email message (for example, the user wants to request a quota increase), the reply is sent 
    to the user specified in the <b>MailReplyTo</b> 
    property. If <b>MailReplyTo</b> is not set, the 
    reply is sent to the user specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactionemail-get_mailfrom">MailFrom</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail2">IFsrmActionEmail2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
