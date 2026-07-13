---
UID: NF:azroles.IAzScope.DeletePolicyReaderName
title: IAzScope::DeletePolicyReaderName (azroles.h)
description: The DeletePolicyReaderName method of IAzScope removes the specified account name from the list of principals that act as policy readers.
helpviewer_keywords: ["AzScope object [Security]","DeletePolicyReaderName method","DeletePolicyReaderName","DeletePolicyReaderName method [Security]","DeletePolicyReaderName method [Security]","AzScope object","DeletePolicyReaderName method [Security]","IAzScope interface","IAzScope interface [Security]","DeletePolicyReaderName method","IAzScope.DeletePolicyReaderName","IAzScope::DeletePolicyReaderName","azroles/IAzScope::DeletePolicyReaderName","security.iazscope_deletepolicyreadername"]
old-location: security\iazscope_deletepolicyreadername.htm
tech.root: security
ms.assetid: e65af2a2-c7f7-483c-af05-342075218158
ms.date: 03/20/2023
ms.keywords: AzScope object [Security],DeletePolicyReaderName method, DeletePolicyReaderName, DeletePolicyReaderName method [Security], DeletePolicyReaderName method [Security],AzScope object, DeletePolicyReaderName method [Security],IAzScope interface, IAzScope interface [Security],DeletePolicyReaderName method, IAzScope.DeletePolicyReaderName, IAzScope::DeletePolicyReaderName, azroles/IAzScope::DeletePolicyReaderName, security.iazscope_deletepolicyreadername
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzScope::DeletePolicyReaderName
 - azroles/IAzScope::DeletePolicyReaderName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzScope.DeletePolicyReaderName
 - AzScope.DeletePolicyReaderName
---

# IAzScope::DeletePolicyReaderName

## -description

The **DeletePolicyReaderName** method removes the specified account name from the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Account name to remove from the list of policy readers. The account name can be in either user principal name (UPN) format (for example, `someone@example.com`) or in the `ExampleDomain\UserName` format. If the domain is not in the `ExampleDomain\UserName` format, the [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the [AccessCheck](nf-azroles-iazclientcontext-accesscheck.md) method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the [PolicyReadersName](nf-azroles-iazscope-get_policyreadersname.md) property.

## -see-also

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)

[AccessCheck](nf-azroles-iazclientcontext-accesscheck.md)
