---
UID: NN:fsrm.IFsrmActionEmail
title: IFsrmActionEmail (fsrm.h)
description: Used to send an email message in response to a quota or file screen event.
helpviewer_keywords: ["IFsrmActionEmail","IFsrmActionEmail interface [File Server Resource Manager]","IFsrmActionEmail interface [File Server Resource Manager]","described","fs.ifsrmactionemail","fsrm.ifsrmactionemail","fsrm/IFsrmActionEmail"]
old-location: fsrm\ifsrmactionemail.htm
tech.root: fsrm
ms.assetid: 6eb6d82e-018d-4977-ad60-fce296c16e83
ms.date: 12/05/2018
ms.keywords: IFsrmActionEmail, IFsrmActionEmail interface [File Server Resource Manager], IFsrmActionEmail interface [File Server Resource Manager],described, fs.ifsrmactionemail, fsrm.ifsrmactionemail, fsrm/IFsrmActionEmail
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmActionEmail
 - fsrm/IFsrmActionEmail
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
 - IFsrmActionEmail
---

# IFsrmActionEmail interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to send an email message in response to a quota or file screen event.

To create an email action, call one of the following methods and specify 
    <b>FsrmActionType_Email</b> as the action type:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>The create methods return an <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. To get 
    this interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method 
    and specify <b>IID_IFsrmActionEmail</b> as the interface identifier.

For file management jobs, see the <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail2">IFsrmActionEmail2</a> 
    interface.

## -remarks

You must set the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactionemail-get_mailto">MailTo</a> and 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactionemail-get_messagetext">MessageText</a> properties; the other 
    properties are optional.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioneventlog">IFsrmActionEventLog</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionreport">IFsrmActionReport</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>