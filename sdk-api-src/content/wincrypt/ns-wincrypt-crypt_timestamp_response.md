---
UID: NS:wincrypt._CRYPT_TIMESTAMP_RESPONSE
title: CRYPT_TIMESTAMP_RESPONSE (wincrypt.h)
description: Is used internally to encapsulate an Abstract Syntax Notation One (ASN.1) Distinguished Encoding Rules (DER) encoded response.
helpviewer_keywords: ["*PCRYPT_TIMESTAMP_RESPONSE","CRYPT_TIMESTAMP_RESPONSE","CRYPT_TIMESTAMP_RESPONSE structure [Security]","PCRYPT_TIMESTAMP_RESPONSE","PCRYPT_TIMESTAMP_RESPONSE structure pointer [Security]","TIMESTAMP_FAILURE_BAD_ALG","TIMESTAMP_FAILURE_BAD_FORMAT","TIMESTAMP_FAILURE_BAD_REQUEST","TIMESTAMP_FAILURE_EXTENSION_NOT_SUPPORTED","TIMESTAMP_FAILURE_INFO_NOT_AVAILABLE","TIMESTAMP_FAILURE_POLICY_NOT_SUPPORTED","TIMESTAMP_FAILURE_SYSTEM_FAILURE","TIMESTAMP_FAILURE_TIME_NOT_AVAILABLE","TIMESTAMP_STATUS_GRANTED","TIMESTAMP_STATUS_GRANTED_WITH_MODS","TIMESTAMP_STATUS_REJECTED","TIMESTAMP_STATUS_REVOCATION_WARNING","TIMESTAMP_STATUS_REVOKED","TIMESTAMP_STATUS_WAITING","security.crypt_timestamp_response","wincrypt/CRYPT_TIMESTAMP_RESPONSE","wincrypt/PCRYPT_TIMESTAMP_RESPONSE"]
old-location: security\crypt_timestamp_response.htm
tech.root: security
ms.assetid: 81647cb7-e5da-4a8b-a50f-83bedd9c0aba
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIMESTAMP_RESPONSE, CRYPT_TIMESTAMP_RESPONSE, CRYPT_TIMESTAMP_RESPONSE structure [Security], PCRYPT_TIMESTAMP_RESPONSE, PCRYPT_TIMESTAMP_RESPONSE structure pointer [Security], TIMESTAMP_FAILURE_BAD_ALG, TIMESTAMP_FAILURE_BAD_FORMAT, TIMESTAMP_FAILURE_BAD_REQUEST, TIMESTAMP_FAILURE_EXTENSION_NOT_SUPPORTED, TIMESTAMP_FAILURE_INFO_NOT_AVAILABLE, TIMESTAMP_FAILURE_POLICY_NOT_SUPPORTED, TIMESTAMP_FAILURE_SYSTEM_FAILURE, TIMESTAMP_FAILURE_TIME_NOT_AVAILABLE, TIMESTAMP_STATUS_GRANTED, TIMESTAMP_STATUS_GRANTED_WITH_MODS, TIMESTAMP_STATUS_REJECTED, TIMESTAMP_STATUS_REVOCATION_WARNING, TIMESTAMP_STATUS_REVOKED, TIMESTAMP_STATUS_WAITING, security.crypt_timestamp_response, wincrypt/CRYPT_TIMESTAMP_RESPONSE, wincrypt/PCRYPT_TIMESTAMP_RESPONSE'
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
req.typenames: CRYPT_TIMESTAMP_RESPONSE, *PCRYPT_TIMESTAMP_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIMESTAMP_RESPONSE
 - wincrypt/_CRYPT_TIMESTAMP_RESPONSE
 - PCRYPT_TIMESTAMP_RESPONSE
 - wincrypt/PCRYPT_TIMESTAMP_RESPONSE
 - CRYPT_TIMESTAMP_RESPONSE
 - wincrypt/CRYPT_TIMESTAMP_RESPONSE
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
 - CRYPT_TIMESTAMP_RESPONSE
---

# CRYPT_TIMESTAMP_RESPONSE structure


## -description

The <b>CRYPT_TIMESTAMP_RESPONSE</b> structure is used internally to encapsulate  an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded response.

## -struct-fields

### -field dwStatus

A <b>DWORD</b> value that indicates the status of the time stamp response.


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_STATUS_GRANTED"></a><a id="timestamp_status_granted"></a><dl>
<dt><b>TIMESTAMP_STATUS_GRANTED</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A TimeStampToken  is present in the <b>ContentInfo</b> member.


</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_STATUS_GRANTED_WITH_MODS"></a><a id="timestamp_status_granted_with_mods"></a><dl>
<dt><b>TIMESTAMP_STATUS_GRANTED_WITH_MODS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A TimeStampToken,
           with modifications, is present in the <b>ContentInfo</b> member.


</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_STATUS_REJECTED"></a><a id="timestamp_status_rejected"></a><dl>
<dt><b>TIMESTAMP_STATUS_REJECTED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The time stamp request was rejected.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_STATUS_WAITING"></a><a id="timestamp_status_waiting"></a><dl>
<dt><b>TIMESTAMP_STATUS_WAITING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The time stamp request is still pending.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_STATUS_REVOCATION_WARNING"></a><a id="timestamp_status_revocation_warning"></a><dl>
<dt><b>TIMESTAMP_STATUS_REVOCATION_WARNING</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The message in the <b>ContentInfo</b> member contains a warning that a revocation is imminent
.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_STATUS_REVOKED"></a><a id="timestamp_status_revoked"></a><dl>
<dt><b>TIMESTAMP_STATUS_REVOKED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The message in the <b>ContentInfo</b> member is a notification that a revocation has occurred.

</td>
</tr>
</table>

### -field cFreeText

Optional. The length, in characters, of the string pointed to by the <b>rgFreeText</b> member.

### -field rgFreeText

Optional. A pointer to a string that contains the text information about request failure.

### -field FailureInfo

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a> structure that contains the reason why the time stamp request was rejected. Each flag is encoded as a bit in the structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_BAD_ALG"></a><a id="timestamp_failure_bad_alg"></a><dl>
<dt><b>TIMESTAMP_FAILURE_BAD_ALG</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An unrecognized or unsupported algorithm identifier was specified.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_BAD_REQUEST"></a><a id="timestamp_failure_bad_request"></a><dl>
<dt><b>TIMESTAMP_FAILURE_BAD_REQUEST</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The transaction is not permitted or supported.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_BAD_FORMAT"></a><a id="timestamp_failure_bad_format"></a><dl>
<dt><b>TIMESTAMP_FAILURE_BAD_FORMAT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The data submitted is in the wrong format.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_TIME_NOT_AVAILABLE"></a><a id="timestamp_failure_time_not_available"></a><dl>
<dt><b>TIMESTAMP_FAILURE_TIME_NOT_AVAILABLE</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The Time Stamping Authority (TSA) time source is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_POLICY_NOT_SUPPORTED"></a><a id="timestamp_failure_policy_not_supported"></a><dl>
<dt><b>TIMESTAMP_FAILURE_POLICY_NOT_SUPPORTED</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The requested TSA policy is not supported by the TSA.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_EXTENSION_NOT_SUPPORTED"></a><a id="timestamp_failure_extension_not_supported"></a><dl>
<dt><b>TIMESTAMP_FAILURE_EXTENSION_NOT_SUPPORTED</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The requested extension is not supported by the TSA.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_INFO_NOT_AVAILABLE"></a><a id="timestamp_failure_info_not_available"></a><dl>
<dt><b>TIMESTAMP_FAILURE_INFO_NOT_AVAILABLE</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The additional information requested was not recognized or is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_FAILURE_SYSTEM_FAILURE"></a><a id="timestamp_failure_system_failure"></a><dl>
<dt><b>TIMESTAMP_FAILURE_SYSTEM_FAILURE</b></dt>
<dt>25</dt>
</dl>
</td>
<td width="60%">
The request cannot be handled due to a system failure.  

</td>
</tr>
</table>

### -field ContentInfo

A <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DER_BLOB</a> structure that encapsulates a signed data content type in Cryptographic Message Syntax (CMS) format.