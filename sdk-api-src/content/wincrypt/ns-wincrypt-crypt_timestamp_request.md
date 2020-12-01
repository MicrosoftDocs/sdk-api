---
UID: NS:wincrypt._CRYPT_TIMESTAMP_REQUEST
title: CRYPT_TIMESTAMP_REQUEST (wincrypt.h)
description: Defines a time stamp request structure that corresponds to the Abstract Syntax Notation One (ASN.1) definition of a TimeStampReq type.
helpviewer_keywords: ["*PCRYPT_TIMESTAMP_REQUEST","CRYPT_TIMESTAMP_REQUEST","CRYPT_TIMESTAMP_REQUEST structure [Security]","PCRYPT_TIMESTAMP_REQUEST","PCRYPT_TIMESTAMP_REQUEST structure pointer [Security]","TIMESTAMP_VERSION","security.crypt_timestamp_request","wincrypt/CRYPT_TIMESTAMP_REQUEST","wincrypt/PCRYPT_TIMESTAMP_REQUEST"]
old-location: security\crypt_timestamp_request.htm
tech.root: security
ms.assetid: 1576986c-1a9b-4fcf-9dab-987b472a8671
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIMESTAMP_REQUEST, CRYPT_TIMESTAMP_REQUEST, CRYPT_TIMESTAMP_REQUEST structure [Security], PCRYPT_TIMESTAMP_REQUEST, PCRYPT_TIMESTAMP_REQUEST structure pointer [Security], TIMESTAMP_VERSION, security.crypt_timestamp_request, wincrypt/CRYPT_TIMESTAMP_REQUEST, wincrypt/PCRYPT_TIMESTAMP_REQUEST'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: CRYPT_TIMESTAMP_REQUEST, *PCRYPT_TIMESTAMP_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIMESTAMP_REQUEST
 - wincrypt/_CRYPT_TIMESTAMP_REQUEST
 - PCRYPT_TIMESTAMP_REQUEST
 - wincrypt/PCRYPT_TIMESTAMP_REQUEST
 - CRYPT_TIMESTAMP_REQUEST
 - wincrypt/CRYPT_TIMESTAMP_REQUEST
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
 - CRYPT_TIMESTAMP_REQUEST
---

# CRYPT_TIMESTAMP_REQUEST structure


## -description

The <b>CRYPT_TIMESTAMP_REQUEST</b> structure defines a time stamp request structure that corresponds to the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) definition of a <b>TimeStampReq</b> type. The <b>CRYPT_TIMESTAMP_REQUEST</b> structure is used internally.

## -struct-fields

### -field dwVersion

A <b>DWORD</b> value that specifies the version of the time stamp request.


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_VERSION"></a><a id="timestamp_version"></a><dl>
<dt><b>TIMESTAMP_VERSION</b></dt>
<dt>	1</dt>
</dl>
</td>
<td width="60%">
A version 1 time stamp request.

</td>
</tr>
</table>

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains information about the algorithm used to calculate the hash.

### -field HashedMessage

A <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DER_BLOB</a> structure that specifies the hash values to be time stamped.

### -field pszTSAPolicyId

Optional. A pointer to a null-terminated string that specifies the Time Stamping Authority (TSA) policy under which the time stamp token should be provided.

### -field Nonce

Optional. A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the nonce value used by the client to verify the
timeliness of the response when no local clock is available.

### -field fCertReq

A Boolean value that indicates whether the TSA must include the certificates used to sign the time stamp token in the response.

### -field cExtension

The number of elements in the array pointed to by the <b>rgExtension</b> member.

### -field rgExtension

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures that contain extension information that is passed in the request.