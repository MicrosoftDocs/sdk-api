---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyReaderName
title: IAzAuthorizationStore::AddPolicyReaderName (azroles.h)
description: Adds the specified account name to the list of principals that act as policy readers. (IAzAuthorizationStore.AddPolicyReaderName)
helpviewer_keywords: ["AddPolicyReaderName","AddPolicyReaderName method [Security]","AddPolicyReaderName method [Security]","AzAuthorizationStore object","AddPolicyReaderName method [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","AddPolicyReaderName method","IAzAuthorizationStore interface [Security]","AddPolicyReaderName method","IAzAuthorizationStore.AddPolicyReaderName","IAzAuthorizationStore::AddPolicyReaderName","azroles/IAzAuthorizationStore::AddPolicyReaderName","security.azauthorizationstore_addpolicyreadername"]
old-location: security\azauthorizationstore_addpolicyreadername.htm
tech.root: security
ms.assetid: 3b111542-61d6-4e5d-abf8-0af61161c885
ms.date: 12/05/2018
ms.keywords: AddPolicyReaderName, AddPolicyReaderName method [Security], AddPolicyReaderName method [Security],AzAuthorizationStore object, AddPolicyReaderName method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyReaderName method, IAzAuthorizationStore interface [Security],AddPolicyReaderName method, IAzAuthorizationStore.AddPolicyReaderName, IAzAuthorizationStore::AddPolicyReaderName, azroles/IAzAuthorizationStore::AddPolicyReaderName, security.azauthorizationstore_addpolicyreadername
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
 - IAzAuthorizationStore::AddPolicyReaderName
 - azroles/IAzAuthorizationStore::AddPolicyReaderName
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
 - AzAuthorizationStore.AddPolicyReaderName
 - IAzAuthorizationStore.AddPolicyReaderName
---

# IAzAuthorizationStore::AddPolicyReaderName


## -description

The <b>AddPolicyReaderName</b> method adds the specified account name to the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Account name to add to the list of policy readers. The account name must be in <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN) format (for example, "someone@example.com"). The <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the  <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyreadersname">PolicyReadersName</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method to persist any changes made by this method.
