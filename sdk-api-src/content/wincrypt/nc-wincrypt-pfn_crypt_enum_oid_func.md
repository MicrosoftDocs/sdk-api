---
UID: NC:wincrypt.PFN_CRYPT_ENUM_OID_FUNC
title: PFN_CRYPT_ENUM_OID_FUNC (wincrypt.h)
description: The CRYPT_ENUM_OID_FUNCTION callback function is used with the CryptEnumOIDFunction function.
helpviewer_keywords: ["CRYPT_ENUM_OID_FUNC","CRYPT_ENUM_OID_FUNCTION","CRYPT_ENUM_OID_FUNCTION callback function [Security]","PFN_CRYPT_ENUM_OID_FUNC","PFN_CRYPT_ENUM_OID_FUNC callback","security.crypt_enum_oid_function","wincrypt/CRYPT_ENUM_OID_FUNCTION"]
old-location: security\crypt_enum_oid_function.htm
tech.root: security
ms.assetid: f29a3454-fa64-4305-ba4e-027d45014024
ms.date: 12/05/2018
ms.keywords: CRYPT_ENUM_OID_FUNC, CRYPT_ENUM_OID_FUNCTION, CRYPT_ENUM_OID_FUNCTION callback function [Security], PFN_CRYPT_ENUM_OID_FUNC, PFN_CRYPT_ENUM_OID_FUNC callback, security.crypt_enum_oid_function, wincrypt/CRYPT_ENUM_OID_FUNCTION
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_ENUM_OID_FUNC
 - wincrypt/PFN_CRYPT_ENUM_OID_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ENUM_OID_FUNCTION
---

# PFN_CRYPT_ENUM_OID_FUNC callback function


## -description

The <b>CRYPT_ENUM_OID_FUNCTION</b> callback function  is used with the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumoidfunction">CryptEnumOIDFunction</a> function.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type to match. Setting this parameter to CRYPT_MATCH_ANY_ENCODING_TYPE matches any encoding type.

<div class="alert"><b>Note</b>  If CRYPT_MATCH_ANY_ENCODING_TYPE is not specified, either a certificate or message encoding type is required.</div>
<div> </div>
If the low-order word containing the certificate encoding type is nonzero, it is used. Otherwise, the high-order word containing the message encoding type is used. If both are specified, the certificate encoding type in the low-order word is used. Currently defined encoding types are:

<ul>
<li>CRYPT_ASN_ENCODING</li>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
<li>CRYPT_MATCH_ANY_ENCODING_TYPE</li>
</ul>

### -param pszFuncName

### -param pszOID [in]

A pointer to either an OID string, such as "2.5.29.1", 
				  an ASCII string, such as "file", or a numeric string, 
				  such as #2000.

### -param cValue [in]

Count of elements in the array of value types.

### -param rgdwValueType[]

### -param rgpwszValueName[]

### -param rgpbValueData[]

### -param rgcbValueData[]

### -param pvArg [in]

A pointer to arguments passed through to the callback function.


#### - pszFunctionName [in]

Name of the OID function.


#### - rgcbValueData [in]

Array that specifies the size, in bytes, of corresponding elements of the <i>rgpbValueData</i> array.


#### - rgdwValueType [in]

Array of value types. Each entry in the array will be one of the value types 
listed for <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionvalue">CryptGetOIDFunctionValue</a> under <i>pdwValueType</i>.


#### - rgpbValueData [in]

Array  containing the values corresponding to the names in the <i>rgpwszValueName</i> array.


#### - rgpwszValueName [in]

Array of null-terminated strings containing the names of the values.

## -returns

Returns <b>TRUE</b> if the function succeeds, <b>FALSE</b> if it fails.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumoidfunction">CryptEnumOIDFunction</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionvalue">CryptGetOIDFunctionValue</a>
