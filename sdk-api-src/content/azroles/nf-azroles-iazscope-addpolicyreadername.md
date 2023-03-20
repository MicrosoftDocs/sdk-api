---
UID: NF:azroles.IAzScope.AddPolicyReaderName
title: IAzScope::AddPolicyReaderName (azroles.h)
description: The AddPolicyReaderName method of IAzScope adds the specified account name to the list of principals that act as policy readers.
helpviewer_keywords: ["AddPolicyReaderName","AddPolicyReaderName method [Security]","AddPolicyReaderName method [Security]","AzScope object","AddPolicyReaderName method [Security]","IAzScope interface","AzScope object [Security]","AddPolicyReaderName method","IAzScope interface [Security]","AddPolicyReaderName method","IAzScope.AddPolicyReaderName","IAzScope::AddPolicyReaderName","azroles/IAzScope::AddPolicyReaderName","security.iazscope_addpolicyreadername"]
old-location: security\iazscope_addpolicyreadername.htm
tech.root: security
ms.assetid: 6beb02cb-7977-4f3f-b806-420c81f6f0b5
ms.date: 03/20/2023
ms.keywords: AddPolicyReaderName, AddPolicyReaderName method [Security], AddPolicyReaderName method [Security],AzScope object, AddPolicyReaderName method [Security],IAzScope interface, AzScope object [Security],AddPolicyReaderName method, IAzScope interface [Security],AddPolicyReaderName method, IAzScope.AddPolicyReaderName, IAzScope::AddPolicyReaderName, azroles/IAzScope::AddPolicyReaderName, security.iazscope_addpolicyreadername
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
 - IAzScope::AddPolicyReaderName
 - azroles/IAzScope::AddPolicyReaderName
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
 - IAzScope.AddPolicyReaderName
 - AzScope.AddPolicyReaderName
---

# IAzScope::AddPolicyReaderName

## -description

The **AddPolicyReaderName** method adds the specified account name to the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Account name to add to the list of policy readers. The account name can be in either user principal name (UPN) format (for example, `someone@example.com`) or in the `ExampleDomain\UserName` format. If the domain is not in the `ExampleDomain\UserName` format, the [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the [AccessCheck](nf-azroles-iazclientcontext-accesscheck.md) method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the [PolicyReadersName](nf-azroles-iazscope-get_policyreadersname.md) property.

You must call the [Submit](nf-azroles-iazscope-submit.md) method to persist any changes made by this method.

## -see-also

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)

[AccessCheck](nf-azroles-iazclientcontext-accesscheck.md)

[Submit](nf-azroles-iazscope-submit.md)
