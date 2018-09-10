---
UID: NF:fsrmquota.IFsrmQuotaObject.get_UserSid
title: IFsrmQuotaObject::get_UserSid
author: windows-sdk-content
description: Retrieves the string form of the user's security identifier (SID) that is associated with the object.
old-location: fsrm\ifsrmquotaobject_usersid.htm
tech.root: fsrm
ms.assetid: f6eed71b-4d14-471a-a686-f7a2be7bf63b
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmQuotaObject interface [File Server Resource Manager],UserSid property, IFsrmQuotaObject.UserSid, IFsrmQuotaObject.get_UserSid, IFsrmQuotaObject::UserSid, IFsrmQuotaObject::get_UserSid, UserSid property [File Server Resource Manager], UserSid property [File Server Resource Manager],IFsrmQuotaObject interface, fs.ifsrmquotaobject_usersid, fsrm.ifsrmquotaobject_usersid, fsrmquota/IFsrmQuotaObject::UserSid, fsrmquota/IFsrmQuotaObject::get_UserSid, get_UserSid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaObject::get_UserSid


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the string form of the user's security identifier (SID) that is associated with the 
    object.

This property is read-only.


## -parameters


## -remarks



This method always returns the well-known SID of 
    <a href="https://msdn.microsoft.com/6f1fa59e-17c0-412b-937b-ddf746ed68bd">WinNULLSid</a>.




## -see-also




<a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

