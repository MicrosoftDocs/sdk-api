---
UID: NF:azroles.IAzApplication.AddPolicyReaderName
title: IAzApplication::AddPolicyReaderName (azroles.h)
description: Adds the specified account name to the list of principals that act as policy readers. (IAzApplication.AddPolicyReaderName)
helpviewer_keywords: ["AddPolicyReaderName","AddPolicyReaderName method [Security]","AddPolicyReaderName method [Security]","AzApplication object","AddPolicyReaderName method [Security]","IAzApplication interface","AzApplication object [Security]","AddPolicyReaderName method","IAzApplication interface [Security]","AddPolicyReaderName method","IAzApplication.AddPolicyReaderName","IAzApplication::AddPolicyReaderName","azroles/IAzApplication::AddPolicyReaderName","security.iazapplication_addpolicyreadername"]
old-location: security\iazapplication_addpolicyreadername.htm
tech.root: security
ms.assetid: cc81527a-7a38-4c5c-857e-bedcda5a5ac3
ms.date: 12/05/2018
ms.keywords: AddPolicyReaderName, AddPolicyReaderName method [Security], AddPolicyReaderName method [Security],AzApplication object, AddPolicyReaderName method [Security],IAzApplication interface, AzApplication object [Security],AddPolicyReaderName method, IAzApplication interface [Security],AddPolicyReaderName method, IAzApplication.AddPolicyReaderName, IAzApplication::AddPolicyReaderName, azroles/IAzApplication::AddPolicyReaderName, security.iazapplication_addpolicyreadername
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
 - IAzApplication::AddPolicyReaderName
 - azroles/IAzApplication::AddPolicyReaderName
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
 - IAzApplication.AddPolicyReaderName
 - AzApplication.AddPolicyReaderName
---

# IAzApplication::AddPolicyReaderName


## -description

The <b>AddPolicyReaderName</b> method adds the specified account name to the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Account name to add to the list of policy readers. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyreadersname">PolicyReadersName</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a> method to persist any changes made by this method.
