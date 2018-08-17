---
UID: NF:wincrypt.CryptSetOIDFunctionValue
title: CryptSetOIDFunctionValue function
author: windows-sdk-content
description: The CryptSetOIDFunctionValue function sets a value for the specified encoding type, function name, OID, and value name.
old-location: security\cryptsetoidfunctionvalue.htm
old-project: SecCrypto
ms.assetid: 3e167c5d-0000-4359-a7b0-9b3e4e64c50c
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CryptSetOIDFunctionValue, CryptSetOIDFunctionValue function [Security], REG_DWORD, REG_EXPAND_SZ, REG_MULTI_SZ, REG_SZ, _crypto2_cryptsetoidfunctionvalue, security.cryptsetoidfunctionvalue, wincrypt/CryptSetOIDFunctionValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
 - CryptSetOIDFunctionValue
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptSetOIDFunctionValue function


## -description


The <b>CryptSetOIDFunctionValue</b> function sets a value for the specified encoding type, function name, OID, and value name.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param pszFuncName [in]

Name of the function for which the encoding type, OID, and value name is being updated.


### -param pszOID [in]

If the high-order word of the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) is nonzero, <i>pszOID</i> is a pointer to either an OID string such as "2.5.29.1" or an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string such as "file". If the high-order word of the OID is zero, the low-order word specifies the integer identifier to be used as the object identifier.


### -param pwszValueName [in]

A pointer to a Unicode string containing the name of the value to set. If a value with this name is not already present, the function creates it.


### -param dwValueType [in]

Specifies the type of information to be stored as the value's data. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_DWORD"></a><a id="reg_dword"></a><dl>
<dt><b>REG_DWORD</b></dt>
</dl>
</td>
<td width="60%">
A 32-bit number.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_EXPAND_SZ"></a><a id="reg_expand_sz"></a><dl>
<dt><b>REG_EXPAND_SZ</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated Unicode string that contains unexpanded references to environment variables (for example, "%PATH%").

</td>
</tr>
<tr>
<td width="40%"><a id="REG_MULTI_SZ"></a><a id="reg_multi_sz"></a><dl>
<dt><b>REG_MULTI_SZ</b></dt>
</dl>
</td>
<td width="60%">
An array of null-terminated Unicode strings, terminated by two <b>NULL</b> characters.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_SZ"></a><a id="reg_sz"></a><dl>
<dt><b>REG_SZ</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated Unicode string.

</td>
</tr>
</table>
 


### -param pbValueData [in]

Points to a buffer containing the data to be stored for the specified value name.


### -param cbValueData [in]

Specifies the size, in bytes, of the information pointed to by the <i>pbValueData</i> parameter. If the data is of type REG_SZ, REG_EXPAND_SZ, or REG_MULTI_SZ, the size must include the terminating <b>NULL</b> wide character.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).




## -see-also




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

