---
UID: NF:azroles.IAzAuthorizationStore.DeletePolicyAdministratorName
title: IAzAuthorizationStore::DeletePolicyAdministratorName
author: windows-sdk-content
description: Removes the specified account name from the list of principals that act as policy administrators.
old-location: security\azauthorizationstore_deletepolicyadministratorname.htm
tech.root: secauthz
ms.assetid: 28be14c8-9e39-4410-a08c-b52bb63d0ce4
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AzAuthorizationStore object [Security],DeletePolicyAdministratorName method, DeletePolicyAdministratorName, DeletePolicyAdministratorName method [Security], DeletePolicyAdministratorName method [Security],AzAuthorizationStore object, DeletePolicyAdministratorName method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeletePolicyAdministratorName method, IAzAuthorizationStore.DeletePolicyAdministratorName, IAzAuthorizationStore::DeletePolicyAdministratorName, azroles/IAzAuthorizationStore::DeletePolicyAdministratorName, security.azauthorizationstore_deletepolicyadministratorname
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
 - AzAuthorizationStore.DeletePolicyAdministratorName
 - IAzAuthorizationStore.DeletePolicyAdministratorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::DeletePolicyAdministratorName


## -description


The <b>DeletePolicyAdministratorName</b> method removes the specified account name from the list of principals that act as policy administrators.


## -parameters




### -param bstrAdmin [in]

The account name to remove from the list of policy administrators. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> function is called to retrieve the domain.


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



