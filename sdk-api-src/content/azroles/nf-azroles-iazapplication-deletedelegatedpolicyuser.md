---
UID: NF:azroles.IAzApplication.DeleteDelegatedPolicyUser
title: IAzApplication::DeleteDelegatedPolicyUser (azroles.h)
author: windows-sdk-content
description: The IAzApplication::DeleteDelegatedPolicyUser method removes the specified security identifier in text form from the list of principals that act as delegated policy users.
old-location: security\iazapplication_deletedelegatedpolicyuser.htm
tech.root: SecAuthZ
ms.assetid: 92e7f4fa-ff86-4ef5-8b87-086dd73966d1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AzApplication object [Security],DeleteDelegatedPolicyUser method, DeleteDelegatedPolicyUser, DeleteDelegatedPolicyUser method [Security], DeleteDelegatedPolicyUser method [Security],AzApplication object, DeleteDelegatedPolicyUser method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteDelegatedPolicyUser method, IAzApplication.DeleteDelegatedPolicyUser, IAzApplication::DeleteDelegatedPolicyUser, azroles/IAzApplication::DeleteDelegatedPolicyUser, security.iazapplication_deletedelegatedpolicyuser
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.DeleteDelegatedPolicyUser
 - AzApplication.DeleteDelegatedPolicyUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::DeleteDelegatedPolicyUser


## -description


The <b>DeleteDelegatedPolicyUser</b> method removes the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a>  (SID) in text form from the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Text form of the SID to remove from the list of delegated policy users.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="https://msdn.microsoft.com/b20e1d5c-b07e-4f75-8b63-38036b07b24d">DelegatedPolicyUsers</a> property.



