---
UID: NF:azroles.IAzScope.AddPolicyReader
title: IAzScope::AddPolicyReader (azroles.h)
description: The AddPolicyReader method of IAzScope adds the specified security identifier in text form to the list of principals that act as policy readers.
helpviewer_keywords: ["AddPolicyReader","AddPolicyReader method [Security]","AddPolicyReader method [Security]","AzScope object","AddPolicyReader method [Security]","IAzScope interface","AzScope object [Security]","AddPolicyReader method","IAzScope interface [Security]","AddPolicyReader method","IAzScope.AddPolicyReader","IAzScope::AddPolicyReader","azroles/IAzScope::AddPolicyReader","security.iazscope_addpolicyreader"]
old-location: security\iazscope_addpolicyreader.htm
tech.root: security
ms.assetid: dd4d3254-8bcf-46b5-8e7b-d3f076988a7c
ms.date: 03/20/2023
ms.keywords: AddPolicyReader, AddPolicyReader method [Security], AddPolicyReader method [Security],AzScope object, AddPolicyReader method [Security],IAzScope interface, AzScope object [Security],AddPolicyReader method, IAzScope interface [Security],AddPolicyReader method, IAzScope.AddPolicyReader, IAzScope::AddPolicyReader, azroles/IAzScope::AddPolicyReader, security.iazscope_addpolicyreader
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
 - IAzScope::AddPolicyReader
 - azroles/IAzScope::AddPolicyReader
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
 - IAzScope.AddPolicyReader
 - AzScope.AddPolicyReader
---

# IAzScope::AddPolicyReader

## -description

The **AddPolicyReader** method adds the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form to the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Text form of the SID to add to the list of policy readers.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the [AccessCheck](nf-azroles-iazclientcontext-accesscheck.md) method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the [PolicyReaders](nf-azroles-iazscope-get_policyreaders.md) property.

You must call the [Submit](nf-azroles-iazscope-submit.md) method to persist any changes made by this method.

## -see-also

[AccessCheck](nf-azroles-iazclientcontext-accesscheck.md)

[PolicyReaders](nf-azroles-iazscope-get_policyreaders.md)

[Submit](nf-azroles-iazscope-submit.md)
