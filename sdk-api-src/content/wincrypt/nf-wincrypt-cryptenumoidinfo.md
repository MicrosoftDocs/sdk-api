---
UID: NF:wincrypt.CryptEnumOIDInfo
title: CryptEnumOIDInfo function (wincrypt.h)
description: Enumerates predefined and registered object identifier (OID) CRYPT_OID_INFO structures. This function enumerates either all of the predefined and registered structures or only structures identified by a selected OID group.
helpviewer_keywords: ["CryptEnumOIDInfo","CryptEnumOIDInfo function [Security]","_crypto2_cryptenumoidinfo","security.cryptenumoidinfo","wincrypt/CryptEnumOIDInfo"]
old-location: security\cryptenumoidinfo.htm
tech.root: security
ms.assetid: 6af23bb4-3a27-425a-90bb-9a69ea081b25
ms.date: 12/05/2018
ms.keywords: CryptEnumOIDInfo, CryptEnumOIDInfo function [Security], _crypto2_cryptenumoidinfo, security.cryptenumoidinfo, wincrypt/CryptEnumOIDInfo
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
 - CryptEnumOIDInfo
 - wincrypt/CryptEnumOIDInfo
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
 - CryptEnumOIDInfo
---

# CryptEnumOIDInfo function


## -description

The <b>CryptEnumOIDInfo</b> function enumerates predefined and registered <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structures. This function enumerates either all of the predefined and registered structures or only structures identified by a selected OID group. For each OID information structure enumerated, an application provided callback function, <i>pfnEnumOIDInfo</i>, is called.

## -parameters

### -param dwGroupId [in]

Indicates which OID groups to be matched. Setting <i>dwGroupId</i> to zero matches all groups. If <i>dwGroupId</i> is greater than zero, only the OID entries in the specified group are enumerated. 




The currently defined OID group IDs are:

<ul>
<li>CRYPT_HASH_ALG_OID_GROUP_ID</li>
<li>CRYPT_ENCRYPT_ALG_OID_GROUP_ID</li>
<li>CRYPT_PUBKEY_ALG_OID_GROUP_ID</li>
<li>CRYPT_SIGN_ALG_OID_GROUP_ID</li>
<li>CRYPT_RDN_ATTR_OID_GROUP_ID</li>
<li>CRYPT_EXT_OR_ATTR_OID_GROUP_ID</li>
<li>CRYPT_ENHKEY_USAGE_OID_GROUP_ID</li>
<li>CRYPT_POLICY_OID_GROUP_ID</li>
<li>CRYPT_TEMPLATE_OID_GROUP_ID</li>
<li>CRYPT_KDF_OID_GROUP_ID <b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The CRYPT_KDF_OID_GROUP_ID value is not supported.

</li>
<li>CRYPT_LAST_OID_GROUP_ID</li>
<li>CRYPT_FIRST_ALG_OID_GROUP_ID</li>
<li>CRYPT_LAST_ALG_OID_GROUP_ID</li>
</ul>

### -param dwFlags [in]

This parameter is reserved for future use. It must be zero.

### -param pvArg [in]

A pointer to arguments to be passed through to the callback function.

### -param pfnEnumOIDInfo [in]

A pointer to the callback function that is executed for each OID information entry enumerated. For information about the callback parameters, see <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info">CRYPT_ENUM_OID_INFO</a>.

## -returns

If the callback function  completes the enumeration, this function returns <b>TRUE</b>. 

If the callback function has stopped the enumeration, this function returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>