---
UID: NF:wincrypt.CryptGetOIDFunctionValue
title: CryptGetOIDFunctionValue function (wincrypt.h)
description: The CryptGetOIDFunctionValue function queries a value associated with an OID.
helpviewer_keywords: ["CryptGetOIDFunctionValue","CryptGetOIDFunctionValue function [Security]","REG_DWORD","REG_EXPAND_SZ","REG_MULTI_SZ","REG_SZ","_crypto2_cryptgetoidfunctionvalue","security.cryptgetoidfunctionvalue","wincrypt/CryptGetOIDFunctionValue"]
old-location: security\cryptgetoidfunctionvalue.htm
tech.root: security
ms.assetid: 14eb7f10-f42a-4496-9699-62eeb9878ea2
ms.date: 12/05/2018
ms.keywords: CryptGetOIDFunctionValue, CryptGetOIDFunctionValue function [Security], REG_DWORD, REG_EXPAND_SZ, REG_MULTI_SZ, REG_SZ, _crypto2_cryptgetoidfunctionvalue, security.cryptgetoidfunctionvalue, wincrypt/CryptGetOIDFunctionValue
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
 - CryptGetOIDFunctionValue
 - wincrypt/CryptGetOIDFunctionValue
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
 - CryptGetOIDFunctionValue
---

# CryptGetOIDFunctionValue function


## -description

The <b>CryptGetOIDFunctionValue</b> function queries a value associated with an OID. The query is made for a specific named value associated with an OID, function name, and encoding type. The function can return the type of queried value, the value, itself, or both.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use    X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param pszFuncName [in]

A pointer to the null-terminated string that contains the name of the OID function set.

### -param pszOID [in]

If the high-order word of the OID is nonzero, <i>pszOID</i> is a pointer to either a  null-terminated OID string such as "2.5.29.1" or a null-terminated <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> string such as "file." If the high-order word of the OID is zero, the low-order word specifies the numeric identifier to be used as the object identifier.

### -param pwszValueName [in]

A pointer to a null-terminated Unicode string that contains the name of the value to be queried.

### -param pdwValueType [out]

A pointer to a variable to receive the value's type. The type returned through this parameter will be one of the following.

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
A Unicode string that contains unexpanded references to environment variables such as "%PATH%". Applications should ensure that the string has a terminating null character before using it. For details about when the string does not have a terminating null character, see <a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_MULTI_SZ"></a><a id="reg_multi_sz"></a><dl>
<dt><b>REG_MULTI_SZ</b></dt>
</dl>
</td>
<td width="60%">
An array of null-terminated Unicode strings. Applications should ensure that the array is properly terminated by two null characters before using it. For details about when the array is not  terminated by two null characters, see <a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_SZ"></a><a id="reg_sz"></a><dl>
<dt><b>REG_SZ</b></dt>
</dl>
</td>
<td width="60%">
A Unicode string. Applications should ensure that the string has a terminating null character before using it. For details about when the string does not have a terminating null character, see <a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>.

</td>
</tr>
</table>
 

The <i>pdwValueType</i> parameter can be <b>NULL</b> if a returned type is not required.

### -param pbValueData [out]

A pointer to a buffer to receive the value associated with the <i>pwszValueName</i> parameter. The buffer must be big enough to contain the terminating <b>NULL</b> character. This parameter can be <b>NULL</b> if returned data is not required.

This parameter can also be <b>NULL</b> to find the size of the buffer for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbValueData [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbValueData</i>.

In most cases the value returned in *<i>pcbValueData</i> includes the size of the terminating <b>NULL</b> character in the string.  For information about situations where the <b>NULL</b> character is not included, see the Remarks section of <a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

This function has the following error code.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbValueData</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbValueData</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>