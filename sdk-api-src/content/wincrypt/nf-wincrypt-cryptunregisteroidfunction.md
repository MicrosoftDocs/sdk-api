---
UID: NF:wincrypt.CryptUnregisterOIDFunction
title: CryptUnregisterOIDFunction function
author: windows-sdk-content
description: Removes the registration of a DLL that contains the function to be called for the specified encoding type, function name, and OID.
old-location: security\cryptunregisteroidfunction.htm
old-project: seccrypto
ms.assetid: c06ffda5-df7c-4e0e-bf4f-8b8c968fcd4c
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CryptUnregisterOIDFunction, CryptUnregisterOIDFunction function [Security], _crypto2_cryptunregisteroidfunction, security.cryptunregisteroidfunction, wincrypt/CryptUnregisterOIDFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - CryptUnregisterOIDFunction
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptUnregisterOIDFunction function


## -description



			The <b>CryptUnregisterOIDFunction</b> function removes the registration of a DLL that contains the function to be called for the specified encoding type, function name, and OID.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are used; however, additional encoding types may be added in the future. To match both current encoding types, use: 



X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

For functions that do not use an encoding type, set this parameter to zero.


### -param pszFuncName [in]

Name of the function being unregistered.


### -param pszOID [in]

A pointer to the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that corresponds to the name of the function being unregistered. If the high order word of the OID is nonzero, <i>pszOID</i> is a pointer to either an OID string such as "2.5.29.1" or an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string such as "file." If the high order word of the OID is zero, the low order word specifies the integer identifier to be used as the object identifier.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/library/Aa380252(v=VS.85).aspx">OID Support Functions</a>
 

 

