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

# _CRYPT_XML_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_VALUE</b> structure contains a single <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> that may be useful in validating the signature.


## -struct-fields




### -field dwType

Specifies the key value type. 


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEY_VALUE_TYPE_DSA"></a><a id="crypt_xml_key_value_type_dsa"></a><dl>
<dt><b>CRYPT_XML_KEY_VALUE_TYPE_DSA</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The key is a DSA key.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEY_VALUE_TYPE_RSA"></a><a id="crypt_xml_key_value_type_rsa"></a><dl>
<dt><b>CRYPT_XML_KEY_VALUE_TYPE_RSA</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The key is an <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a> key.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEY_VALUE_TYPE_ECDSA"></a><a id="crypt_xml_key_value_type_ecdsa"></a><dl>
<dt><b>CRYPT_XML_KEY_VALUE_TYPE_ECDSA</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The key is an Elliptic Curve Digital Signature Algorithm (ECDSA) key.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEY_VALUE_TYPE_CUSTOM"></a><a id="crypt_xml_key_value_type_custom"></a><dl>
<dt><b>CRYPT_XML_KEY_VALUE_TYPE_CUSTOM</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The key is a custom key type.

</td>
</tr>
</table>
 


### -field DSAKeyValue

A <a href="https://msdn.microsoft.com/634c47c2-28ba-40ea-975d-95f5663eb0b0">CRYPT_XML_KEY_DSA_KEY_VALUE</a> structure that contains <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) key data.


### -field RSAKeyValue

A <a href="https://msdn.microsoft.com/e2b1344d-c108-4255-bd50-06d742ed67a8">CRYPT_XML_KEY_RSA_KEY_VALUE</a> structure that contains RSA key data.


### -field ECDSAKeyValue

A <a href="https://msdn.microsoft.com/db7e8ee0-25b4-4e2e-83da-f970906c9da9">CRYPT_XML_KEY_ECDSA_KEY_VALUE</a> structure that contains ECDSA key data.


### -field Custom

A <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure that contains custom key data.

