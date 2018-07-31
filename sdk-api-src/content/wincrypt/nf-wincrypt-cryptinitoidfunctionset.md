---
UID: NF:wincrypt.CryptInitOIDFunctionSet
title: CryptInitOIDFunctionSet function
author: windows-sdk-content
description: The CryptInitOIDFunctionSet initializes and returns the handle of the OID function set identified by a supplied function set name.
old-location: security\cryptinitoidfunctionset.htm
old-project: SecCrypto
ms.assetid: 576a2989-ed7f-417d-b60e-24baf90a6554
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CryptInitOIDFunctionSet, CryptInitOIDFunctionSet function [Security], _crypto2_cryptinitoidfunctionset, security.cryptinitoidfunctionset, wincrypt/CryptInitOIDFunctionSet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptInitOIDFunctionSet
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

