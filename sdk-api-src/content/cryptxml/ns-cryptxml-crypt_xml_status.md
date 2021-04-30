---
UID: NS:cryptxml._CRYPT_XML_STATUS
title: CRYPT_XML_STATUS (cryptxml.h)
description: Returns information about the signature validation status, summary status information about a SignedInfo element, or summary status information about an array of Reference elements.
helpviewer_keywords: ["*PCRYPT_XML_STATUS","CRYPT_XML_STATUS","CRYPT_XML_STATUS structure [Security]","CRYPT_XML_STATUS_DIGESTING","CRYPT_XML_STATUS_DIGEST_VALID","CRYPT_XML_STATUS_ERROR_DIGEST_INVALID","CRYPT_XML_STATUS_ERROR_KEYINFO_NOT_PARSED","CRYPT_XML_STATUS_ERROR_NOT_RESOLVED","CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_ALGORITHM","CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_TRANSFORM","CRYPT_XML_STATUS_ERROR_SIGNATURE_INVALID","CRYPT_XML_STATUS_INTERNAL_REFERENCE","CRYPT_XML_STATUS_KEY_AVAILABLE","CRYPT_XML_STATUS_OPENED_TO_ENCODE","CRYPT_XML_STATUS_SIGNATURE_VALID","PCRYPT_XML_STATUS","PCRYPT_XML_STATUS structure pointer [Security]","cryptxml/CRYPT_XML_STATUS","cryptxml/PCRYPT_XML_STATUS","security.crypt_xml_status"]
old-location: security\crypt_xml_status.htm
tech.root: security
ms.assetid: 1d49429e-9c81-4bf0-92d8-4effe9795dc9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_STATUS, CRYPT_XML_STATUS, CRYPT_XML_STATUS structure [Security], CRYPT_XML_STATUS_DIGESTING, CRYPT_XML_STATUS_DIGEST_VALID, CRYPT_XML_STATUS_ERROR_DIGEST_INVALID, CRYPT_XML_STATUS_ERROR_KEYINFO_NOT_PARSED, CRYPT_XML_STATUS_ERROR_NOT_RESOLVED, CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_ALGORITHM, CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_TRANSFORM, CRYPT_XML_STATUS_ERROR_SIGNATURE_INVALID, CRYPT_XML_STATUS_INTERNAL_REFERENCE, CRYPT_XML_STATUS_KEY_AVAILABLE, CRYPT_XML_STATUS_OPENED_TO_ENCODE, CRYPT_XML_STATUS_SIGNATURE_VALID, PCRYPT_XML_STATUS, PCRYPT_XML_STATUS structure pointer [Security], cryptxml/CRYPT_XML_STATUS, cryptxml/PCRYPT_XML_STATUS, security.crypt_xml_status'
req.header: cryptxml.h
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
req.typenames: CRYPT_XML_STATUS, *PCRYPT_XML_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_STATUS
 - cryptxml/_CRYPT_XML_STATUS
 - PCRYPT_XML_STATUS
 - cryptxml/PCRYPT_XML_STATUS
 - CRYPT_XML_STATUS
 - cryptxml/CRYPT_XML_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_STATUS
---

# CRYPT_XML_STATUS structure


## -description

The <b>CRYPT_XML_STATUS</b> structure returns information about the signature validation status, 
  summary status information about a <b>SignedInfo</b> element, or summary status information 
  about an array of <b>Reference</b> elements. The <b>CRYPT_XML_STATUS</b> structure is used by the <a href="/windows/desktop/api/cryptxml/nf-cryptxml-cryptxmlgetstatus">CryptXmlGetStatus</a> function.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwErrorStatus

The retrieved error flags.


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_ERROR_NOT_RESOLVED"></a><a id="crypt_xml_status_error_not_resolved"></a><dl>
<dt><b>CRYPT_XML_STATUS_ERROR_NOT_RESOLVED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
One of the references could not be resolved.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_ERROR_DIGEST_INVALID"></a><a id="crypt_xml_status_error_digest_invalid"></a><dl>
<dt><b>CRYPT_XML_STATUS_ERROR_DIGEST_INVALID</b></dt>
<dt>0x0000002</dt>
</dl>
</td>
<td width="60%">
The digest value could not be verified.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_ALGORITHM"></a><a id="crypt_xml_status_error_not_supported_algorithm"></a><dl>
<dt><b>CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_ALGORITHM</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
One of the algorithm URIs specified in XML is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_TRANSFORM"></a><a id="crypt_xml_status_error_not_supported_transform"></a><dl>
<dt><b>CRYPT_XML_STATUS_ERROR_NOT_SUPPORTED_TRANSFORM</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
One of the transform URIs specified in XML is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_ERROR_SIGNATURE_INVALID"></a><a id="crypt_xml_status_error_signature_invalid"></a><dl>
<dt><b>CRYPT_XML_STATUS_ERROR_SIGNATURE_INVALID</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The signature value could not be verified.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_ERROR_KEYINFO_NOT_PARSED"></a><a id="crypt_xml_status_error_keyinfo_not_parsed"></a><dl>
<dt><b>CRYPT_XML_STATUS_ERROR_KEYINFO_NOT_PARSED</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Unable to parse the <b>KeyInfo</b> element.

</td>
</tr>
</table>

### -field dwInfoStatus

The retrieved informational flags.


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_INTERNAL_REFERENCE"></a><a id="crypt_xml_status_internal_reference"></a><dl>
<dt><b>CRYPT_XML_STATUS_INTERNAL_REFERENCE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The reference URI points to an internal element in XML 
and can be resolved automatically.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_KEY_AVAILABLE"></a><a id="crypt_xml_status_key_available"></a><dl>
<dt><b>CRYPT_XML_STATUS_KEY_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>KeyValue</b> element parsed, and a key handle imported successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_DIGESTING"></a><a id="crypt_xml_status_digesting"></a><dl>
<dt><b>CRYPT_XML_STATUS_DIGESTING</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The reference is being added to the digest.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_DIGEST_VALID"></a><a id="crypt_xml_status_digest_valid"></a><dl>
<dt><b>CRYPT_XML_STATUS_DIGEST_VALID</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The digest value was verified.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_SIGNATURE_VALID"></a><a id="crypt_xml_status_signature_valid"></a><dl>
<dt><b>CRYPT_XML_STATUS_SIGNATURE_VALID</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The signature value was verified.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_STATUS_OPENED_TO_ENCODE"></a><a id="crypt_xml_status_opened_to_encode"></a><dl>
<dt><b>CRYPT_XML_STATUS_OPENED_TO_ENCODE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The document is open for encoding.

</td>
</tr>
</table>