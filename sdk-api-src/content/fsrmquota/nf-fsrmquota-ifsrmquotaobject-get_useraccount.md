---
UID: NF:fsrmquota.IFsrmQuotaObject.get_UserAccount
title: IFsrmQuotaObject::get_UserAccount (fsrmquota.h)
description: Retrieves the string form of the user account that is associated with the object.
helpviewer_keywords: ["IFsrmQuotaObject interface [File Server Resource Manager]","UserAccount property","IFsrmQuotaObject.UserAccount","IFsrmQuotaObject.get_UserAccount","IFsrmQuotaObject::UserAccount","IFsrmQuotaObject::get_UserAccount","UserAccount property [File Server Resource Manager]","UserAccount property [File Server Resource Manager]","IFsrmQuotaObject interface","fs.ifsrmquotaobject_useraccount","fsrm.ifsrmquotaobject_useraccount","fsrmquota/IFsrmQuotaObject::UserAccount","fsrmquota/IFsrmQuotaObject::get_UserAccount","get_UserAccount"]
old-location: fsrm\ifsrmquotaobject_useraccount.htm
tech.root: fsrm
ms.assetid: 02545dfb-6c71-4412-9376-81c9304efaa8
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaObject interface [File Server Resource Manager],UserAccount property, IFsrmQuotaObject.UserAccount, IFsrmQuotaObject.get_UserAccount, IFsrmQuotaObject::UserAccount, IFsrmQuotaObject::get_UserAccount, UserAccount property [File Server Resource Manager], UserAccount property [File Server Resource Manager],IFsrmQuotaObject interface, fs.ifsrmquotaobject_useraccount, fsrm.ifsrmquotaobject_useraccount, fsrmquota/IFsrmQuotaObject::UserAccount, fsrmquota/IFsrmQuotaObject::get_UserAccount, get_UserAccount
req.header: fsrmquota.h
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
 - IFsrmQuotaObject::get_UserAccount
 - fsrmquota/IFsrmQuotaObject::get_UserAccount
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
 - IFsrmQuotaObject.UserAccount
 - IFsrmQuotaObject.get_UserAccount
---

# IFsrmQuotaObject::get_UserAccount


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the string form of the user account that is associated with the object.

This property is read-only.

## -parameters

## -remarks

This method always returns the string form of the account that corresponds to the well-known SID of 
    <a href="/windows/desktop/api/winnt/ne-winnt-well_known_sid_type">WinNULLSid</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>