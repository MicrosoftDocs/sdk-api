---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyAdministratorName
title: IAzAuthorizationStore::AddPolicyAdministratorName
author: windows-sdk-content
description: Adds the specified account name to the list of principals that act as policy administrators.
old-location: security\azauthorizationstore_addpolicyadministratorname.htm
tech.root: secauthz
ms.assetid: b77348c7-4389-47ba-9f4f-e5643cf992aa
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AddPolicyAdministratorName, AddPolicyAdministratorName method [Security], AddPolicyAdministratorName method [Security],AzAuthorizationStore object, AddPolicyAdministratorName method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyAdministratorName method, IAzAuthorizationStore interface [Security],AddPolicyAdministratorName method, IAzAuthorizationStore.AddPolicyAdministratorName, IAzAuthorizationStore::AddPolicyAdministratorName, azroles/IAzAuthorizationStore::AddPolicyAdministratorName, security.azauthorizationstore_addpolicyadministratorname
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
 - AzAuthorizationStore.AddPolicyAdministratorName
 - IAzAuthorizationStore.AddPolicyAdministratorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzAuthorizationStore.AddPolicyAdministratorName
: 
---

# IAzAuthorizationStore::AddPolicyAdministratorName


## -description


The <b>AddPolicyAdministratorName</b> method adds the specified account name to the list of principals that act as policy administrators.

This method is an alternate version of the <a href="https://msdn.microsoft.com/8d73bc05-1366-4b47-9eaf-4a247ebf8d93">AddPolicyAdministrator</a> method.


## -parameters




### -param bstrAdmin [in]

Account name  to add to the list of policy administrators. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Policy administrators for an object can perform the following tasks:

<ul>
<li>Read the object</li>
<li>Write attributes to the object</li>
<li>Read attributes of child objects of the object</li>
<li>Write attributes to child objects of the object</li>
<li>Delete the object</li>
<li>Delete child objects of the object</li>
<li>Create child objects of the object</li>
</ul>
To view the list of policy administrators in account name format, use the <a href="https://msdn.microsoft.com/20f84f75-ad27-4329-90a8-46e7d817863f">PolicyAdministratorsName</a> property.

You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



