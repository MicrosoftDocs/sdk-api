---
UID: NF:azroles.IAzClientContext3.GetOperations
title: IAzClientContext3::GetOperations (azroles.h)
description: Returns a collection of the operations, within the specified scope, that the principal represented by the current client context has permission to perform.
helpviewer_keywords: ["GetOperations","GetOperations method [Security]","GetOperations method [Security]","IAzClientContext3 interface","IAzClientContext3 interface [Security]","GetOperations method","IAzClientContext3.GetOperations","IAzClientContext3::GetOperations","azroles/IAzClientContext3::GetOperations","security.iazclientcontext3_getoperations_method"]
old-location: security\iazclientcontext3_getoperations_method.htm
tech.root: security
ms.assetid: 0f5c7e2d-e88d-4236-888c-9bf5a425713c
ms.date: 12/05/2018
ms.keywords: GetOperations, GetOperations method [Security], GetOperations method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],GetOperations method, IAzClientContext3.GetOperations, IAzClientContext3::GetOperations, azroles/IAzClientContext3::GetOperations, security.iazclientcontext3_getoperations_method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzClientContext3::GetOperations
 - azroles/IAzClientContext3::GetOperations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzClientContext3.GetOperations
---

# IAzClientContext3::GetOperations


## -description

The <b>GetOperations</b> method returns a collection of the operations, within the specified scope, that the principal represented by the current client context has permission to perform.

## -parameters

### -param bstrScopeName [in]

The name of the scope to check.

### -param ppOperationCollection [out]

The address of a pointer to the collection of operations that the principal represented by the current client context has permission to perform.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.