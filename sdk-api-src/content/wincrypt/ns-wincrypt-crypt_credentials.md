---
UID: NS:wincrypt._CRYPT_CREDENTIALS
title: CRYPT_CREDENTIALS (wincrypt.h)
description: Contains information about credentials that can be passed as optional input to a remote object retrieval function such as CryptRetrieveObjectByUrl or CryptGetTimeValidObject.
helpviewer_keywords: ["*PCRYPT_CREDENTIALS","CREDENTIAL_OID_PASSWORD_CREDENTIALS","CRYPT_CREDENTIALS","CRYPT_CREDENTIALS structure [Security]","PCRYPT_CREDENTIALS","PCRYPT_CREDENTIALS structure pointer [Security]","security.crypt_credentials","wincrypt/CRYPT_CREDENTIALS","wincrypt/PCRYPT_CREDENTIALS"]
old-location: security\crypt_credentials.htm
tech.root: security
ms.assetid: d28b2f52-3258-44ad-a3ab-0743d3afcd62
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CREDENTIALS, CREDENTIAL_OID_PASSWORD_CREDENTIALS, CRYPT_CREDENTIALS, CRYPT_CREDENTIALS structure [Security], PCRYPT_CREDENTIALS, PCRYPT_CREDENTIALS structure pointer [Security], security.crypt_credentials, wincrypt/CRYPT_CREDENTIALS, wincrypt/PCRYPT_CREDENTIALS'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CRYPT_CREDENTIALS, *PCRYPT_CREDENTIALS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CREDENTIALS
 - wincrypt/_CRYPT_CREDENTIALS
 - PCRYPT_CREDENTIALS
 - wincrypt/PCRYPT_CREDENTIALS
 - CRYPT_CREDENTIALS
 - wincrypt/CRYPT_CREDENTIALS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_CREDENTIALS
---

# CRYPT_CREDENTIALS structure


## -description

The <b>CRYPT_CREDENTIALS</b> structure contains information about credentials that can be passed as optional input to a remote object retrieval function such as <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgettimevalidobject">CryptGetTimeValidObject</a>.

## -struct-fields

### -field cbSize

The size in bytes of this structure.

### -field pszCredentialsOid

A pointer to a null-terminated string that contains the type of credential object represented by the <b>pvCredentials</b> member.


This member can contain the following possible value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREDENTIAL_OID_PASSWORD_CREDENTIALS"></a><a id="credential_oid_password_credentials"></a><dl>
<dt><b>CREDENTIAL_OID_PASSWORD_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
The <b>pvCredentials</b> member contains a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_password_credentialsa">CRYPT_PASSWORD_CREDENTIALS</a> structure that represents a user name and password combination.

</td>
</tr>
</table>

### -field pvCredentials

A pointer to a structure as defined by the <b>pszCredentialsOid</b> member.