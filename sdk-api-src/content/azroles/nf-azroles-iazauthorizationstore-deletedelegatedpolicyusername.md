---
UID: NF:azroles.IAzAuthorizationStore.DeleteDelegatedPolicyUserName
title: IAzAuthorizationStore::DeleteDelegatedPolicyUserName
author: windows-sdk-content
description: Removes the specified account name from the list of principals that act as delegated policy users.
old-location: security\azauthorizationstore_deletedelegatedpolicyusername.htm
tech.root: SecAuthZ
ms.assetid: a2e7523a-41d3-4fb5-b455-588e0618f51f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AzAuthorizationStore object [Security],DeleteDelegatedPolicyUserName method, DeleteDelegatedPolicyUserName, DeleteDelegatedPolicyUserName method [Security], DeleteDelegatedPolicyUserName method [Security],AzAuthorizationStore object, DeleteDelegatedPolicyUserName method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteDelegatedPolicyUserName method, IAzAuthorizationStore.DeleteDelegatedPolicyUserName, IAzAuthorizationStore::DeleteDelegatedPolicyUserName, azroles/IAzAuthorizationStore::DeleteDelegatedPolicyUserName, security.azauthorizationstore_deletedelegatedpolicyusername
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
 - AzAuthorizationStore.DeleteDelegatedPolicyUserName
 - IAzAuthorizationStore.DeleteDelegatedPolicyUserName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::DeleteDelegatedPolicyUserName


## -description


The <b>DeleteDelegatedPolicyUserName</b> method removes the specified account name from the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Account name to remove from the list of delegated policy users. The account name must be in <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

An attempt to call this method on an XML store will return E_INVALIDARG.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a>  or <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users in account name format, use the <a href="https://msdn.microsoft.com/495cdba4-7127-48aa-9542-7ccbedbad589">DelegatedPolicyUsersName</a> property.



