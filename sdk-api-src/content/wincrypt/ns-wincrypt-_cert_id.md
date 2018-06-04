---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

