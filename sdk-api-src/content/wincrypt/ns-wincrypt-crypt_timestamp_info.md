---
UID: NS:wincrypt._CRYPT_TIMESTAMP_INFO
title: CRYPT_TIMESTAMP_INFO (wincrypt.h)
description: Contains a signed data content type in Cryptographic Message Syntax (CMS) format.
helpviewer_keywords: ["*PCRYPT_TIMESTAMP_INFO","CRYPT_TIMESTAMP_INFO","CRYPT_TIMESTAMP_INFO structure [Security]","PCRYPT_TIMESTAMP_INFO","PCRYPT_TIMESTAMP_INFO structure pointer [Security]","TIMESTAMP_VERSION","security.crypt_timestamp_info","wincrypt/CRYPT_TIMESTAMP_INFO","wincrypt/PCRYPT_TIMESTAMP_INFO"]
old-location: security\crypt_timestamp_info.htm
tech.root: security
ms.assetid: 05ca0877-5e9d-4b21-9fca-a1eef2cb4626
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIMESTAMP_INFO, CRYPT_TIMESTAMP_INFO, CRYPT_TIMESTAMP_INFO structure [Security], PCRYPT_TIMESTAMP_INFO, PCRYPT_TIMESTAMP_INFO structure pointer [Security], TIMESTAMP_VERSION, security.crypt_timestamp_info, wincrypt/CRYPT_TIMESTAMP_INFO, wincrypt/PCRYPT_TIMESTAMP_INFO'
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
req.typenames: CRYPT_TIMESTAMP_INFO, *PCRYPT_TIMESTAMP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIMESTAMP_INFO
 - wincrypt/_CRYPT_TIMESTAMP_INFO
 - PCRYPT_TIMESTAMP_INFO
 - wincrypt/PCRYPT_TIMESTAMP_INFO
 - CRYPT_TIMESTAMP_INFO
 - wincrypt/CRYPT_TIMESTAMP_INFO
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
 - CRYPT_TIMESTAMP_INFO
---

# CRYPT_TIMESTAMP_INFO structure


## -description

The <b>CRYPT_TIMESTAMP_INFO</b> structure contains a signed data content type in Cryptographic Message Syntax (CMS) format.

## -struct-fields

### -field dwVersion

A <b>DWORD</b> value that specifies the version of the time stamp request.

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
Specifies that this is a version 1 time stamp request.

</td>
</tr>
</table>

### -field pszTSAPolicyId

Optional. A pointer to a null-terminated string that specifies the Time Stamping Authority (TSA) policy under which the time stamp token was provided. This value must correspond with the value passed  in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_request">CRYPT_TIMESTAMP_REQUEST</a> structure.

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains information about the algorithm used to calculate the hash. This value must correspond with the value passed  in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_request">CRYPT_TIMESTAMP_REQUEST</a> structure.

### -field HashedMessage

A <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DER_BLOB</a> structure that specifies the hash values to be time stamped.

### -field SerialNumber

 A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the serial number assigned by the TSA to each time stamp token.

### -field ftTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> value that specifies the time at which the time stamp token was produced by the TSA.

### -field pvAccuracy

Optional. A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_accuracy">CRYPT_TIMESTAMP_ACCURACY</a>   structure that contains the time deviation around the UTC time at which the time stamp token was created by the TSA.

### -field fOrdering

This member is reserved.

### -field Nonce

Optional. A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains the nonce value used by the client to verify the
timeliness of the response when no local clock is available. This value must correspond with the value passed  in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_request">CRYPT_TIMESTAMP_REQUEST</a> structure.

### -field Tsa

Optional. A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains the subject name of the TSA certificate.

### -field cExtension

The number of elements in the array pointed to by the <b>rgExtension</b> member.

### -field rgExtension

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures that contain extension information returned from the request.