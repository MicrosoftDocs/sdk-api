---
UID: NF:wincrypt.CryptGetKeyIdentifierProperty
title: CryptGetKeyIdentifierProperty function (wincrypt.h)
description: The CryptGetKeyIdentifierProperty acquires a specific property from a specified key identifier.
helpviewer_keywords: ["CRYPT_KEYID_ALLOC_FLAG","CRYPT_KEYID_MACHINE_FLAG","CryptGetKeyIdentifierProperty","CryptGetKeyIdentifierProperty function [Security]","_crypto2_cryptgetkeyidentifierproperty","security.cryptgetkeyidentifierproperty","wincrypt/CryptGetKeyIdentifierProperty"]
old-location: security\cryptgetkeyidentifierproperty.htm
tech.root: security
ms.assetid: bc0511c1-0699-4959-afd7-a838c91c77d5
ms.date: 12/05/2018
ms.keywords: CRYPT_KEYID_ALLOC_FLAG, CRYPT_KEYID_MACHINE_FLAG, CryptGetKeyIdentifierProperty, CryptGetKeyIdentifierProperty function [Security], _crypto2_cryptgetkeyidentifierproperty, security.cryptgetkeyidentifierproperty, wincrypt/CryptGetKeyIdentifierProperty
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptGetKeyIdentifierProperty
 - wincrypt/CryptGetKeyIdentifierProperty
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
 - CryptGetKeyIdentifierProperty
---

# CryptGetKeyIdentifierProperty function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptGetKeyIdentifierProperty</b> acquires a specific property from a specified key identifier.

## -parameters

### -param pKeyIdentifier [in]

A pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> that contains the key identifier.

### -param dwPropId [in]

Identifies the property to retrieve. The value of <i>dwPropId</i> determines the type and content of the <i>pvData</i> parameter. Any certificate property ID can be used.

### -param dwFlags [in]

The following flags can be used. They can be combined with a bitwise-<b>OR</b> operation. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KEYID_MACHINE_FLAG"></a><a id="crypt_keyid_machine_flag"></a><dl>
<dt><b>CRYPT_KEYID_MACHINE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Search the list of key identifiers of the LocalMachine (if <i>pwszComputerName</i> is <b>NULL</b>) or remote computer (if <i>pwszComputerName</i> is not <b>NULL</b>). For more information, see <i>pwszComputerName</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KEYID_ALLOC_FLAG"></a><a id="crypt_keyid_alloc_flag"></a><dl>
<dt><b>CRYPT_KEYID_ALLOC_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The <b>LocalAlloc()</b> function is called to allocate memory for <i>pvData</i>. *<i>pvData</i> is updated with a pointer to the allocated memory. <b>LocalFree()</b> must be called to free the allocated memory.

</td>
</tr>
</table>

### -param pwszComputerName [in]

A pointer to the name of a remote computer to be searched. If CRYPT_KEYID_MACHINE_FLAG flag is set, searches the remote computer for a list of key identifiers. If the local computer is to be searched and not a remote computer, set <i>pwszComputerName</i> to <b>NULL</b>.

### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.

### -param pvData [out]

A pointer to a buffer to receive the data as determined by <i>dwPropId</i>. Elements pointed to by fields in the <i>pvData</i> structure follow the structure. Therefore, the size contained in <i>pcbData</i> can exceed the size of the structure. 




If <i>dwPropId</i> is CERT_KEY_PROV_INFO_PROP_ID, <i>pvData</i> points to a CRYPT_KEY_PROV_INFO structure that contains the property of the key identifier.

If <i>dwPropId</i> is not CERT_KEY_PROV_INFO_PROP_ID, <i>pvData</i> points to an array of bytes that contains the property of the key identifier.

To get the size of this information for memory allocation purposes, this parameter can be <b>NULL</b> when the CRYPT_KEYID_ALLOC_FLAG is not set. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

When the CRYPT_KEYID_ALLOC_FLAG is set, <i>pvData</i> is the address of a pointer to the buffer that will be updated. Because memory is allocated and its pointer is stored at *<i>pvData</i>, <i>pvData</i> must not be <b>NULL</b>.

### -param pcbData [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. The size contained in the variable pointed to by <i>pcbData</i> can indicate a size larger than the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure because the structure can contain pointers to auxiliary data. This size is the sum of the size needed by the structure and all auxiliary data. 




When the CRYPT_KEYID_ALLOC_FLAG is set, <i>pcbData</i> is the address of a pointer to the <b>DWORD</b> that will be updated.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties">CryptEnumKeyIdentifierProperties</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty">CryptSetKeyIdentifierProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Key Identifier Functions</a>