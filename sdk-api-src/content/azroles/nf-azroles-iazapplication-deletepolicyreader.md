---
UID: NF:azroles.IAzApplication.DeletePolicyReader
title: IAzApplication::DeletePolicyReader (azroles.h)
description: The DeletePolicyReader method of IAzApplication removes the specified security identifier in text form from the list of principals that act as policy readers.
helpviewer_keywords: ["AzApplication object [Security]","DeletePolicyReader method","DeletePolicyReader","DeletePolicyReader method [Security]","DeletePolicyReader method [Security]","AzApplication object","DeletePolicyReader method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeletePolicyReader method","IAzApplication.DeletePolicyReader","IAzApplication::DeletePolicyReader","azroles/IAzApplication::DeletePolicyReader","security.iazapplication_deletepolicyreader"]
old-location: security\iazapplication_deletepolicyreader.htm
tech.root: security
ms.assetid: aec8b5c4-3c5e-4b91-a10f-40ef05beca1f
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],DeletePolicyReader method, DeletePolicyReader, DeletePolicyReader method [Security], DeletePolicyReader method [Security],AzApplication object, DeletePolicyReader method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePolicyReader method, IAzApplication.DeletePolicyReader, IAzApplication::DeletePolicyReader, azroles/IAzApplication::DeletePolicyReader, security.iazapplication_deletepolicyreader
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
 - IAzApplication::DeletePolicyReader
 - azroles/IAzApplication::DeletePolicyReader
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
 - IAzApplication.DeletePolicyReader
 - AzApplication.DeletePolicyReader
---

# IAzApplication::DeletePolicyReader

## -description

The **DeletePolicyReader** method removes the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form from the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Text form of the SID to remove from the list of policy readers.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the [AccessCheck](nf-azroles-iazclientcontext-accesscheck.md) method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the [PolicyReaders](nf-azroles-iazapplication-get_policyreaders.md) property.

## -see-also

[AccessCheck](nf-azroles-iazclientcontext-accesscheck.md)

[PolicyReaders](nf-azroles-iazapplication-get_policyreaders.md)
