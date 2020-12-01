---
UID: NF:wincrypt.CryptEnumKeyIdentifierProperties
title: CryptEnumKeyIdentifierProperties function (wincrypt.h)
description: The CryptEnumKeyIdentifierProperties function enumerates key identifiers and their properties.
helpviewer_keywords: ["CryptEnumKeyIdentifierProperties","CryptEnumKeyIdentifierProperties function [Security]","_crypto2_cryptenumkeyidentifierproperties","security.cryptenumkeyidentifierproperties","wincrypt/CryptEnumKeyIdentifierProperties"]
old-location: security\cryptenumkeyidentifierproperties.htm
tech.root: security
ms.assetid: 6e57d935-4cfb-44af-b1c6-6c399c959452
ms.date: 12/05/2018
ms.keywords: CryptEnumKeyIdentifierProperties, CryptEnumKeyIdentifierProperties function [Security], _crypto2_cryptenumkeyidentifierproperties, security.cryptenumkeyidentifierproperties, wincrypt/CryptEnumKeyIdentifierProperties
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
 - CryptEnumKeyIdentifierProperties
 - wincrypt/CryptEnumKeyIdentifierProperties
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
 - CryptEnumKeyIdentifierProperties
---

# CryptEnumKeyIdentifierProperties function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptEnumKeyIdentifierProperties</b> function enumerates key identifiers and their properties. This function is not called in a loop. Rather, it loops internally until the last key identifier property is enumerated or the callback function returns <b>FALSE</b>. If <i>dwPropId</i> is zero or if the properties of the key identifier match the <i>dwPropId</i>, the callback function is called.

## -parameters

### -param pKeyIdentifier [in, optional]

A pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains the key identifier. 




If <i>pKeyIdentifier</i> is <b>NULL</b>, the function enumerates all key identifiers.

If <i>pKeyIdentifier</i> is not <b>NULL</b>, the callback function <i>pfnEnum</i> is only called for the specified key identifier.

### -param dwPropId [in]

Indicates the property identifier to be listed. 




If <i>dwPropId</i> is set to zero, this function calls the callback function with all the properties.

If <i>dwPropId</i> is not zero and <i>pKeyIdentifier</i> is <b>NULL</b>, the callback function is called only for those key identifiers that have the specified property (sets the <i>cProp</i> parameter of <i>pfnEnum</i> to one). All key identifiers that do not have the property are skipped.

Any certificate property identifier can be used.

### -param dwFlags [in]

By default, the list of key identifiers for the CurrentUser is searched. If CRYPT_KEYID_MACHINE_FLAG is set, the list of key identifiers of the LocalMachine (if <i>pwszComputerName</i> is <b>NULL</b>) or of a remote computer (if <i>pwszComputerName</i> is not <b>NULL</b>) is searched. For more information, see <i>pwszComputerName</i>.

### -param pwszComputerName [in, optional]

A pointer to the name of a remote computer to be searched. If CRYPT_KEYID_MACHINE_FLAG is set in <i>dwFlags</i>, the remote computer is searched for a list of key identifiers. If the local computer is to be searched and not a remote computer, <i>pwszComputerName</i> is set to <b>NULL</b>.

### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.

### -param pvArg [in, optional]

A pointer to data to be passed to the callback function. The type is a void that allows the application to declare, define, and initialize a structure or argument to hold any information.

### -param pfnEnum [in]

A pointer to an application-defined callback function that is executed for each key identifier entry that matches the input parameters. For details about the callback functions parameters, see <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop">CRYPT_ENUM_KEYID_PROP</a>.

## -returns

The <b>CryptEnumKeyIdentifierProperties</b> function repeatedly calls the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop">CRYPT_ENUM_KEYID_PROP</a> callback function until the last key identifier is enumerated or the callback function returns <b>FALSE</b>.

If the main function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

To continue enumeration, the function returns <b>TRUE</b>.

To stop enumeration, the function returns <b>FALSE</b> and sets the last error code.

## -remarks

A key identifier can have the same properties as a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-working-with-key-identifiers">Example C Program: Working with Key Identifiers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Base Cryptography Functions</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty">CryptGetKeyIdentifierProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty">CryptSetKeyIdentifierProperty</a>