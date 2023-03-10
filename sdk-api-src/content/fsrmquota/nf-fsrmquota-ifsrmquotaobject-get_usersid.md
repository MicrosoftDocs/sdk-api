---
UID: NF:fsrmquota.IFsrmQuotaObject.get_UserSid
title: IFsrmQuotaObject::get_UserSid (fsrmquota.h)
description: Retrieves the string form of the user's security identifier (SID) that is associated with the object.
helpviewer_keywords: ["IFsrmQuotaObject interface [File Server Resource Manager]","UserSid property","IFsrmQuotaObject.UserSid","IFsrmQuotaObject.get_UserSid","IFsrmQuotaObject::UserSid","IFsrmQuotaObject::get_UserSid","UserSid property [File Server Resource Manager]","UserSid property [File Server Resource Manager]","IFsrmQuotaObject interface","fs.ifsrmquotaobject_usersid","fsrm.ifsrmquotaobject_usersid","fsrmquota/IFsrmQuotaObject::UserSid","fsrmquota/IFsrmQuotaObject::get_UserSid","get_UserSid"]
old-location: fsrm\ifsrmquotaobject_usersid.htm
tech.root: fsrm
ms.assetid: f6eed71b-4d14-471a-a686-f7a2be7bf63b
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaObject interface [File Server Resource Manager],UserSid property, IFsrmQuotaObject.UserSid, IFsrmQuotaObject.get_UserSid, IFsrmQuotaObject::UserSid, IFsrmQuotaObject::get_UserSid, UserSid property [File Server Resource Manager], UserSid property [File Server Resource Manager],IFsrmQuotaObject interface, fs.ifsrmquotaobject_usersid, fsrm.ifsrmquotaobject_usersid, fsrmquota/IFsrmQuotaObject::UserSid, fsrmquota/IFsrmQuotaObject::get_UserSid, get_UserSid
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
 - IFsrmQuotaObject::get_UserSid
 - fsrmquota/IFsrmQuotaObject::get_UserSid
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
 - IFsrmQuotaObject.UserSid
 - IFsrmQuotaObject.get_UserSid
---

# IFsrmQuotaObject::get_UserSid


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the string form of the user's security identifier (SID) that is associated with the 
    object.

This property is read-only.

## -parameters

## -remarks

This method always returns the well-known SID of 
    <a href="/windows/desktop/api/winnt/ne-winnt-well_known_sid_type">WinNULLSid</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>