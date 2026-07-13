---
UID: NF:azroles.IAzApplication.DeletePolicyReaderName
title: IAzApplication::DeletePolicyReaderName (azroles.h)
description: Removes the specified account name from the list of principals that act as policy readers. (IAzApplication.DeletePolicyReaderName)
helpviewer_keywords: ["AzApplication object [Security]","DeletePolicyReaderName method","DeletePolicyReaderName","DeletePolicyReaderName method [Security]","DeletePolicyReaderName method [Security]","AzApplication object","DeletePolicyReaderName method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeletePolicyReaderName method","IAzApplication.DeletePolicyReaderName","IAzApplication::DeletePolicyReaderName","azroles/IAzApplication::DeletePolicyReaderName","security.iazapplication_deletepolicyreadername"]
old-location: security\iazapplication_deletepolicyreadername.htm
tech.root: security
ms.assetid: 1948fb2d-a1ca-4f66-889d-d00f8f265ba5
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeletePolicyReaderName method, DeletePolicyReaderName, DeletePolicyReaderName method [Security], DeletePolicyReaderName method [Security],AzApplication object, DeletePolicyReaderName method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePolicyReaderName method, IAzApplication.DeletePolicyReaderName, IAzApplication::DeletePolicyReaderName, azroles/IAzApplication::DeletePolicyReaderName, security.iazapplication_deletepolicyreadername
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
 - IAzApplication::DeletePolicyReaderName
 - azroles/IAzApplication::DeletePolicyReaderName
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
 - IAzApplication.DeletePolicyReaderName
 - AzApplication.DeletePolicyReaderName
---

# IAzApplication::DeletePolicyReaderName


## -description

The <b>DeletePolicyReaderName</b> method removes the specified account name from the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

The account name to remove from the list of policy readers. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the format of "ExampleDomain\UserName". If the domain is not  in the "ExampleDomain\UserName" format, the <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyreadersname">PolicyReadersName</a> property.
