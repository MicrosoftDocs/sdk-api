---
UID: NF:wincrypt.CryptInitOIDFunctionSet
title: CryptInitOIDFunctionSet function (wincrypt.h)
description: The CryptInitOIDFunctionSet initializes and returns the handle of the OID function set identified by a supplied function set name.
helpviewer_keywords: ["CryptInitOIDFunctionSet","CryptInitOIDFunctionSet function [Security]","_crypto2_cryptinitoidfunctionset","security.cryptinitoidfunctionset","wincrypt/CryptInitOIDFunctionSet"]
old-location: security\cryptinitoidfunctionset.htm
tech.root: security
ms.assetid: 576a2989-ed7f-417d-b60e-24baf90a6554
ms.date: 12/05/2018
ms.keywords: CryptInitOIDFunctionSet, CryptInitOIDFunctionSet function [Security], _crypto2_cryptinitoidfunctionset, security.cryptinitoidfunctionset, wincrypt/CryptInitOIDFunctionSet
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptInitOIDFunctionSet
 - wincrypt/CryptInitOIDFunctionSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptInitOIDFunctionSet
---

# CryptInitOIDFunctionSet function


## -description

The <b>CryptInitOIDFunctionSet</b> initializes and returns the handle of the OID function set identified by a supplied function set name. If the set already exists, the handle of the existing set is returned. If the set does not exist, it is created. This allows different DLLs to install OID functions for the same function set name.

## -parameters

### -param pszFuncName [in]

Name of the OID function set.

### -param dwFlags [in]

Reserved for future use and must be zero.

## -returns

Returns the handle of the OID function set identified by <i>pszFuncName</i>, or <b>NULL</b> if the function fails.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>