---
UID: NF:azroles.IAzApplication3.CreateScope2
title: IAzApplication3::CreateScope2 (azroles.h)
description: Creates a new IAzScope2 object with the specified name.
helpviewer_keywords: ["CreateScope2","CreateScope2 method [Security]","CreateScope2 method [Security]","IAzApplication3 interface","IAzApplication3 interface [Security]","CreateScope2 method","IAzApplication3.CreateScope2","IAzApplication3::CreateScope2","azroles/IAzApplication3::CreateScope2","security.iazapplication3_createscope2"]
old-location: security\iazapplication3_createscope2.htm
tech.root: security
ms.assetid: f1e8bfe6-e074-4e9e-80f8-bcb8bd90f824
ms.date: 12/05/2018
ms.keywords: CreateScope2, CreateScope2 method [Security], CreateScope2 method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],CreateScope2 method, IAzApplication3.CreateScope2, IAzApplication3::CreateScope2, azroles/IAzApplication3::CreateScope2, security.iazapplication3_createscope2
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzApplication3::CreateScope2
 - azroles/IAzApplication3::CreateScope2
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
 - IAzApplication3.CreateScope2
---

# IAzApplication3::CreateScope2


## -description

The <b>CreateScope2</b> method creates a new <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object with the specified name.

## -parameters

### -param bstrScopeName [in]

A string that contains the name of the new <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object.

### -param ppScope2 [out]

The address of a pointer to the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object that this method creates.

When you have finished using this <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.