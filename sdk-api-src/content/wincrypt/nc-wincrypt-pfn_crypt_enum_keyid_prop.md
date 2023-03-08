---
UID: NC:wincrypt.PFN_CRYPT_ENUM_KEYID_PROP
title: PFN_CRYPT_ENUM_KEYID_PROP (wincrypt.h)
description: The CRYPT_ENUM_KEYID_PROP callback function is used with the CryptEnumKeyIdentifierProperties function.
helpviewer_keywords: ["CRYPT_ENUM_KEYID_PROP","CRYPT_ENUM_KEYID_PROP callback function [Security]","PFN_CRYPT_ENUM_KEYID_PROP","PFN_CRYPT_ENUM_KEYID_PROP callback","security.crypt_enum_keyid_prop","wincrypt/CRYPT_ENUM_KEYID_PROP"]
old-location: security\crypt_enum_keyid_prop.htm
tech.root: security
ms.assetid: c4461b79-d216-4d4a-bd5d-9260ec897c14
ms.date: 12/05/2018
ms.keywords: CRYPT_ENUM_KEYID_PROP, CRYPT_ENUM_KEYID_PROP callback function [Security], PFN_CRYPT_ENUM_KEYID_PROP, PFN_CRYPT_ENUM_KEYID_PROP callback, security.crypt_enum_keyid_prop, wincrypt/CRYPT_ENUM_KEYID_PROP
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
 - PFN_CRYPT_ENUM_KEYID_PROP
 - wincrypt/PFN_CRYPT_ENUM_KEYID_PROP
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
 - CRYPT_ENUM_KEYID_PROP
---

# PFN_CRYPT_ENUM_KEYID_PROP callback function


## -description

The <b>CRYPT_ENUM_KEYID_PROP</b> callback function  is used with the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties">CryptEnumKeyIdentifierProperties</a> function.

## -parameters

### -param pKeyIdentifier [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> that contains the key identifier.

### -param dwFlags [in]

Reserved for future use and must be zero.

### -param pvReserved [in]

Reserved for future use. Must be <b>NULL</b>.

### -param pvArg [in, out]

A pointer to an argument that is passed back from the callback function.

### -param cProp [in]

Count of elements in the array of <i>rgdwPropId</i>

### -param rgdwPropId [in]

A pointer to an array of property identifiers. Each entry in the array will be one of the value types listed for in the table for <i>dwPropId</i> in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty">CryptSetKeyIdentifierProperty</a> function.


#### - **rgpvData [in]

A pointer to an array that contains pointers to <i>pvData</i> elements corresponding the <i>rgdwPropId</i> array elements. 




For CERT_KEY_PROV_INFO_PROP_ID the <i>rgpvData</i> element points to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure. For all other properties, the <i>rgpvData</i> element points to an array of bytes.

### -param rgcbData [in]

Array of <b>DWORD</b>s that specify the size, in bytes, of corresponding elements in the <i>rgpvData</i> array.

### -param rgpvData [in]

A pointer to an array that contains pointers to <i>pvData</i> elements corresponding the <i>rgdwPropId</i> array elements. 




For CERT_KEY_PROV_INFO_PROP_ID the <i>rgpvData</i> element points to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure. For all other properties, the <i>rgpvData</i> element points to an array of bytes.

## -returns

Returns <b>TRUE</b> if the function succeeds, <b>FALSE</b> if it fails.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties">CryptEnumKeyIdentifierProperties</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty">CryptSetKeyIdentifierProperty</a>
