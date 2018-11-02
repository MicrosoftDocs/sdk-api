---
UID: NF:azroles.IAzApplication.AddDelegatedPolicyUserName
title: IAzApplication::AddDelegatedPolicyUserName
author: windows-sdk-content
description: Adds the specified account name to the list of principals that act as delegated policy users.
old-location: security\iazapplication_adddelegatedpolicyusername.htm
tech.root: secauthz
ms.assetid: f30392f6-7100-43dd-ab20-419cd02d9ea5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddDelegatedPolicyUserName, AddDelegatedPolicyUserName method [Security], AddDelegatedPolicyUserName method [Security],AzApplication object, AddDelegatedPolicyUserName method [Security],IAzApplication interface, AzApplication object [Security],AddDelegatedPolicyUserName method, IAzApplication interface [Security],AddDelegatedPolicyUserName method, IAzApplication.AddDelegatedPolicyUserName, IAzApplication::AddDelegatedPolicyUserName, azroles/IAzApplication::AddDelegatedPolicyUserName, security.iazapplication_adddelegatedpolicyusername
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
 - IAzApplication.AddDelegatedPolicyUserName
 - AzApplication.AddDelegatedPolicyUserName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::AddDelegatedPolicyUserName


## -description


The <b>AddDelegatedPolicyUserName</b> method adds the specified account name to the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Account name to add to the list of delegated policy users. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

An attempt to call this method on an XML store will return E_INVALIDARG.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users in account name format, use the <a href="https://msdn.microsoft.com/ee18b86f-7ae2-4984-ac7a-3909eda647e3">DelegatedPolicyUsersName</a> property.

You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



