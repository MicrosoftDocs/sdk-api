---
UID: NF:azroles.IAzAuthorizationStore.AddDelegatedPolicyUser
title: IAzAuthorizationStore::AddDelegatedPolicyUser
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of principals that act as delegated policy users.
old-location: security\azauthorizationstore_adddelegatedpolicyuser.htm
tech.root: SecAuthZ
ms.assetid: 0c6714e9-489e-4266-a8b5-35c66b0a14f4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddDelegatedPolicyUser, AddDelegatedPolicyUser method [Security], AddDelegatedPolicyUser method [Security],AzAuthorizationStore object, AddDelegatedPolicyUser method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddDelegatedPolicyUser method, IAzAuthorizationStore interface [Security],AddDelegatedPolicyUser method, IAzAuthorizationStore.AddDelegatedPolicyUser, IAzAuthorizationStore::AddDelegatedPolicyUser, azroles/IAzAuthorizationStore::AddDelegatedPolicyUser, security.azauthorizationstore_adddelegatedpolicyuser
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - AzAuthorizationStore.AddDelegatedPolicyUser
 - IAzAuthorizationStore.AddDelegatedPolicyUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::AddDelegatedPolicyUser


## -description


The <b>AddDelegatedPolicyUser</b> method adds the specified <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">security identifier</a> (SID) in text form to the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Text form of the SID to add to the list of delegated policy users.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/en-us/library/Aa446684(v=VS.85).aspx">IAzApplication</a>  or <a href="https://msdn.microsoft.com/en-us/library/Aa378237(v=VS.85).aspx">IAzScope</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="https://msdn.microsoft.com/en-us/library/Aa376343(v=VS.85).aspx">DelegatedPolicyUsers</a> property.

You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa376369(v=VS.85).aspx">Submit</a> method to persist any changes made by this method.



