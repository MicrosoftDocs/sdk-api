---
UID: NS:wincrypt._CERT_ID
title: CERT_ID (wincrypt.h)
description: Is used as a flexible means of uniquely identifying a certificate.
helpviewer_keywords: ["*PCERT_ID","CERT_ID","CERT_ID structure [Security]","CERT_ID_ISSUER_SERIAL_NUMBER","CERT_ID_KEY_IDENTIFIER","CERT_ID_SHA1_HASH","PCERT_ID","PCERT_ID structure pointer [Security]","_crypto2_cert_id","security.cert_id","wincrypt/CERT_ID","wincrypt/PCERT_ID"]
old-location: security\cert_id.htm
tech.root: security
ms.assetid: 9e33f661-c365-4725-8c3f-27b6cdd9a84e
ms.date: 12/05/2018
ms.keywords: '*PCERT_ID, CERT_ID, CERT_ID structure [Security], CERT_ID_ISSUER_SERIAL_NUMBER, CERT_ID_KEY_IDENTIFIER, CERT_ID_SHA1_HASH, PCERT_ID, PCERT_ID structure pointer [Security], _crypto2_cert_id, security.cert_id, wincrypt/CERT_ID, wincrypt/PCERT_ID'
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
req.typenames: CERT_ID, *PCERT_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_ID
 - wincrypt/_CERT_ID
 - PCERT_ID
 - wincrypt/PCERT_ID
 - CERT_ID
 - wincrypt/CERT_ID
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
 - CERT_ID
---

# CERT_ID structure


## -description

The <b>CERT_ID</b> structure is used as a flexible means of uniquely identifying a certificate.

## -struct-fields

### -field dwIdChoice

A <b>DWORD</b> value that indicates which member of the union is being used. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_ID_ISSUER_SERIAL_NUMBER"></a><a id="cert_id_issuer_serial_number"></a><dl>
<dt><b>CERT_ID_ISSUER_SERIAL_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
IssuerSerialNumber

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ID_KEY_IDENTIFIER"></a><a id="cert_id_key_identifier"></a><dl>
<dt><b>CERT_ID_KEY_IDENTIFIER</b></dt>
</dl>
</td>
<td width="60%">
KeyId

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ID_SHA1_HASH"></a><a id="cert_id_sha1_hash"></a><dl>
<dt><b>CERT_ID_SHA1_HASH</b></dt>
</dl>
</td>
<td width="60%">
HashId

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.IssuerSerialNumber

A 
							<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_issuer_serial_number">CERT_ISSUER_SERIAL_NUMBER</a> structure that uniquely identifies a certificate.

### -field DUMMYUNIONNAME.KeyId

A 
							<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains a certificate key identifier.

### -field DUMMYUNIONNAME.HashId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> that contains a SHA1 <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the certificate to be used as a unique identifier of the certificate.