---
UID: NF:azroles.IAzAuthorizationStore.DeleteDelegatedPolicyUser
title: IAzAuthorizationStore::DeleteDelegatedPolicyUser
author: windows-driver-content
description: Removes the specified security identifier (SID) in text form from the list of principals that act as delegated policy users.
old-location: security\azauthorizationstore_deletedelegatedpolicyuser.htm
old-project: SecAuthZ
ms.assetid: cb00abca-7116-4a71-aed0-87ed9caff0fb
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzAuthorizationStore object [Security],DeleteDelegatedPolicyUser method, DeleteDelegatedPolicyUser, DeleteDelegatedPolicyUser method [Security], DeleteDelegatedPolicyUser method [Security],AzAuthorizationStore object, DeleteDelegatedPolicyUser method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteDelegatedPolicyUser method, IAzAuthorizationStore.DeleteDelegatedPolicyUser, IAzAuthorizationStore::DeleteDelegatedPolicyUser, azroles/IAzAuthorizationStore::DeleteDelegatedPolicyUser, security.azauthorizationstore_deletedelegatedpolicyuser
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	AzAuthorizationStore.DeleteDelegatedPolicyUser
-	IAzAuthorizationStore.DeleteDelegatedPolicyUser
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::DeleteDelegatedPolicyUser


## -description


The <b>DeleteDelegatedPolicyUser</b> method removes the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Text form of the SID to remove from the list of delegated policy users.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a>  or <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object uses to administer the delegated object. 

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="https://msdn.microsoft.com/cc1268d5-d386-4888-a987-e40896a096e4">DelegatedPolicyUsers</a> property.



