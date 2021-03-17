---
UID: NF:wincrypt.CryptSetKeyIdentifierProperty
title: CryptSetKeyIdentifierProperty function (wincrypt.h)
description: The CryptSetKeyIdentifierProperty function sets the property of a specified key identifier. This function can set the property on the computer identified in pwszComputerName.
helpviewer_keywords: ["CRYPT_KEYID_DELETE_FLAG","CRYPT_KEYID_MACHINE_FLAG","CRYPT_KEYID_SET_NEW_FLAG","CryptSetKeyIdentifierProperty","CryptSetKeyIdentifierProperty function [Security]","_crypto2_cryptsetkeyidentifierproperty","security.cryptsetkeyidentifierproperty","wincrypt/CryptSetKeyIdentifierProperty"]
old-location: security\cryptsetkeyidentifierproperty.htm
tech.root: security
ms.assetid: 0970aaaa-3f9a-4471-bd21-5de8746f94a2
ms.date: 12/05/2018
ms.keywords: CRYPT_KEYID_DELETE_FLAG, CRYPT_KEYID_MACHINE_FLAG, CRYPT_KEYID_SET_NEW_FLAG, CryptSetKeyIdentifierProperty, CryptSetKeyIdentifierProperty function [Security], _crypto2_cryptsetkeyidentifierproperty, security.cryptsetkeyidentifierproperty, wincrypt/CryptSetKeyIdentifierProperty
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
 - CryptSetKeyIdentifierProperty
 - wincrypt/CryptSetKeyIdentifierProperty
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
 - CryptSetKeyIdentifierProperty
---

# CryptSetKeyIdentifierProperty function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetKeyIdentifierProperty</b> function sets the property of a specified key identifier. This function can set the property on the computer identified in <i>pwszComputerName</i>.

## -parameters

### -param pKeyIdentifier [in]

A pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> containing the key identifier.

### -param dwPropId [in]

Identifies the property to be set. The value of <i>dwPropId</i> determines the type and content of the <i>pvData</i> parameter. Any certificate property ID can be used. CERT_KEY_PROV_INFO_PROP_ID is the property of most interest.

### -param dwFlags [in]

The following flags can be set. They can be combined with a bitwise-<b>OR</b> operation.

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
Sets the property of the LocalMachine (if <i>pwszComputerName</i> is <b>NULL</b>) or remote computer (if <i>pwszComputerName</i> is not <b>NULL</b>). For more information, see <i>pwszComputerName</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KEYID_DELETE_FLAG"></a><a id="crypt_keyid_delete_flag"></a><dl>
<dt><b>CRYPT_KEYID_DELETE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The key identifier and all of its properties are deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KEYID_SET_NEW_FLAG"></a><a id="crypt_keyid_set_new_flag"></a><dl>
<dt><b>CRYPT_KEYID_SET_NEW_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Sets a new key identifier property. If the property already exists, the attempt fails, and <b>FALSE</b> is returned with the last error code set to CRYPT_E_EXISTS.

</td>
</tr>
</table>

### -param pwszComputerName [in]

A pointer to a <b>null</b>-terminated string that contains the name of a remote computer that has the key identifier where the properties are set. If CRYPT_KEYID_MACHINE_FLAG flag is set, searches the remote computer for a list of key identifiers. If the local computer is to be set and not a remote computer, set <i>pwszComputerName</i> to <b>NULL</b>.

### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.

### -param pvData [out]

If <i>dwPropId</i> is CERT_KEY_PROV_INFO_PROP_ID, <i>pvData</i> points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure containing the property of the key identifier. 




If <i>dwPropId</i> is not CERT_KEY_PROV_INFO_PROP_ID, <i>pvData</i> points to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure containing the property of the key identifier.

Setting <i>pvData</i> to <b>NULL</b> deletes the property.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  If CRYPT_KEYID_SET_NEW_FLAG is set and the property already exists, <b>FALSE</b> is returned with the last error code set to CRYPT_E_EXISTS.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties">CryptEnumKeyIdentifierProperties</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty">CryptGetKeyIdentifierProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Key Identifier Functions</a>