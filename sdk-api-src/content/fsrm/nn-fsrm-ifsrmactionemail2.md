---
UID: NN:fsrm.IFsrmActionEmail2
title: IFsrmActionEmail2 (fsrm.h)
description: Used to limit the number of expired files listed in the email notification.
helpviewer_keywords: ["IFsrmActionEmail2","IFsrmActionEmail2 interface [File Server Resource Manager]","IFsrmActionEmail2 interface [File Server Resource Manager]","described","fs.ifsrmactionemail2","fsrm.ifsrmactionemail2","fsrm/IFsrmActionEmail2"]
old-location: fsrm\ifsrmactionemail2.htm
tech.root: fsrm
ms.assetid: 278ef98d-fb1d-42a4-a740-07c5e713a230
ms.date: 12/05/2018
ms.keywords: IFsrmActionEmail2, IFsrmActionEmail2 interface [File Server Resource Manager], IFsrmActionEmail2 interface [File Server Resource Manager],described, fs.ifsrmactionemail2, fsrm.ifsrmactionemail2, fsrm/IFsrmActionEmail2
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmActionEmail2
 - fsrm/IFsrmActionEmail2
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
 - IFsrmActionEmail2
---

# IFsrmActionEmail2 interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to limit the number of expired files listed in the email notification.

Use this version of the interface for file management  notifications. To create an email action for file 
    management notifications, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a> 
    method and specify <b>FsrmActionType_Email</b> as the action type.

The 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">CreateNotificationAction</a> 
    method returns an <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. To get this interface, 
    call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method and specify 
    <b>IID_IFsrmActionEmail2</b> as the interface identifier.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>