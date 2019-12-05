---
UID: NF:azroles.IAzAuthorizationStore.DeletePolicyReaderName
title: IAzAuthorizationStore::DeletePolicyReaderName (azroles.h)
description: Removes the specified account name from the list of principals that act as policy readers.
old-location: security\azauthorizationstore_deletepolicyreadername.htm
tech.root: SecAuthZ
ms.assetid: b3375c24-82c3-43fd-a063-8c8079324641
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],DeletePolicyReaderName method, DeletePolicyReaderName, DeletePolicyReaderName method [Security], DeletePolicyReaderName method [Security],AzAuthorizationStore object, DeletePolicyReaderName method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeletePolicyReaderName method, IAzAuthorizationStore.DeletePolicyReaderName, IAzAuthorizationStore::DeletePolicyReaderName, azroles/IAzAuthorizationStore::DeletePolicyReaderName, security.azauthorizationstore_deletepolicyreadername
ms.topic: method
f1_keywords:
- azroles/AzAuthorizationStore.DeletePolicyReaderName
dev_langs:
- c++
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
- AzAuthorizationStore.DeletePolicyReaderName
- IAzAuthorizationStore.DeletePolicyReaderName
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzAuthorizationStore::DeletePolicyReaderName


## -description


The <b>DeletePolicyReaderName</b> method removes the specified account name from the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

The account name to remove from the list of policy readers. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyreadersname">PolicyReadersName</a> property.



