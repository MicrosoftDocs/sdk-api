---
UID: NF:fsrmquota.IFsrmQuotaObject.get_UserAccount
title: IFsrmQuotaObject::get_UserAccount
author: windows-sdk-content
description: Retrieves the string form of the user account that is associated with the object.
old-location: fsrm\ifsrmquotaobject_useraccount.htm
tech.root: fsrm
ms.assetid: 02545dfb-6c71-4412-9376-81c9304efaa8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFsrmQuotaObject interface [File Server Resource Manager],UserAccount property, IFsrmQuotaObject.UserAccount, IFsrmQuotaObject.get_UserAccount, IFsrmQuotaObject::UserAccount, IFsrmQuotaObject::get_UserAccount, UserAccount property [File Server Resource Manager], UserAccount property [File Server Resource Manager],IFsrmQuotaObject interface, fs.ifsrmquotaobject_useraccount, fsrm.ifsrmquotaobject_useraccount, fsrmquota/IFsrmQuotaObject::UserAccount, fsrmquota/IFsrmQuotaObject::get_UserAccount, get_UserAccount
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
 - IFsrmQuotaObject.UserAccount
 - IFsrmQuotaObject.get_UserAccount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaObject::get_UserAccount


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the string form of the user account that is associated with the object.

This property is read-only.


## -parameters


## -remarks



This method always returns the string form of the account that corresponds to the well-known SID of 
    <a href="https://msdn.microsoft.com/6f1fa59e-17c0-412b-937b-ddf746ed68bd">WinNULLSid</a>.




## -see-also




<a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

