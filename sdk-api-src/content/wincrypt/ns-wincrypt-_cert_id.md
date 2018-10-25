---
UID: NS:wincrypt._CERT_ID
title: "_CERT_ID"
author: windows-sdk-content
description: Is used as a flexible means of uniquely identifying a certificate.
old-location: security\cert_id.htm
tech.root: seccrypto
ms.assetid: 9e33f661-c365-4725-8c3f-27b6cdd9a84e
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PCERT_ID, CERT_ID, CERT_ID structure [Security], CERT_ID_ISSUER_SERIAL_NUMBER, CERT_ID_KEY_IDENTIFIER, CERT_ID_SHA1_HASH, PCERT_ID, PCERT_ID structure pointer [Security], _CERT_ID, _crypto2_cert_id, security.cert_id, wincrypt/CERT_ID, wincrypt/PCERT_ID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_ID
product: Windows
targetos: Windows
req.typenames: CERT_ID, *PCERT_ID
req.redist: 
---

# _CERT_ID structure


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
							<a href="https://msdn.microsoft.com/4e44113f-81e7-4551-bf4d-50986d6d57bb">CERT_ISSUER_SERIAL_NUMBER</a> structure that uniquely identifies a certificate.


### -field DUMMYUNIONNAME.KeyId

A 
							<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure that contains a certificate key identifier.


### -field DUMMYUNIONNAME.HashId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> that contains a SHA1 <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the certificate to be used as a unique identifier of the certificate.

