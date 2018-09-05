---
UID: NF:azroles.IAzAuthorizationStore.AddDelegatedPolicyUserName
title: IAzAuthorizationStore::AddDelegatedPolicyUserName
author: windows-sdk-content
description: Adds the specified account name to the list of principals that act as delegated policy users.
old-location: security\azauthorizationstore_adddelegatedpolicyusername.htm
old-project: SecAuthZ
ms.assetid: 9eeb4670-a3be-46dd-83b4-4ab12a311fe3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddDelegatedPolicyUserName, AddDelegatedPolicyUserName method [Security], AddDelegatedPolicyUserName method [Security],AzAuthorizationStore object, AddDelegatedPolicyUserName method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddDelegatedPolicyUserName method, IAzAuthorizationStore interface [Security],AddDelegatedPolicyUserName method, IAzAuthorizationStore.AddDelegatedPolicyUserName, IAzAuthorizationStore::AddDelegatedPolicyUserName, azroles/IAzAuthorizationStore::AddDelegatedPolicyUserName, security.azauthorizationstore_adddelegatedpolicyusername
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
 - AzAuthorizationStore.AddDelegatedPolicyUserName
 - IAzAuthorizationStore.AddDelegatedPolicyUserName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::AddDelegatedPolicyUserName


## -description


The <b>AddDelegatedPolicyUserName</b> method adds the specified account name to the list of principals that act as delegated policy users.
			

This method is an alternate version of the <a href="https://msdn.microsoft.com/0c6714e9-489e-4266-a8b5-35c66b0a14f4">AddDelegatedPolicyUser</a> method.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Account name to add to the list of delegated policy users. The account name must be in <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


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

You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



