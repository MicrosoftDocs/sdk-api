---
UID: NF:azroles.IAzAuthorizationStore.AddDelegatedPolicyUser
title: IAzAuthorizationStore::AddDelegatedPolicyUser
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of principals that act as delegated policy users.
old-location: security\azauthorizationstore_adddelegatedpolicyuser.htm
old-project: secauthz
ms.assetid: 0c6714e9-489e-4266-a8b5-35c66b0a14f4
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: AddDelegatedPolicyUser, AddDelegatedPolicyUser method [Security], AddDelegatedPolicyUser method [Security],AzAuthorizationStore object, AddDelegatedPolicyUser method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddDelegatedPolicyUser method, IAzAuthorizationStore interface [Security],AddDelegatedPolicyUser method, IAzAuthorizationStore.AddDelegatedPolicyUser, IAzAuthorizationStore::AddDelegatedPolicyUser, azroles/IAzAuthorizationStore::AddDelegatedPolicyUser, security.azauthorizationstore_adddelegatedpolicyuser
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::AddDelegatedPolicyUser


## -description


The <b>AddDelegatedPolicyUser</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Text form of the SID to add to the list of delegated policy users.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a>  or <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="https://msdn.microsoft.com/cc1268d5-d386-4888-a987-e40896a096e4">DelegatedPolicyUsers</a> property.

You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



