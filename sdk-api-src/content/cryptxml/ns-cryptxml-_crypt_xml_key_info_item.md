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

# _CRYPT_XML_KEY_INFO_ITEM structure


## -description


The <b>CRYPT_XML_KEY_INFO_ITEM</b> structure encapsulates key information data that corresponds to a <b>KeyInfo</b> element. The <b>KeyInfo</b> element enables 
 the recipient to obtain the key needed to validate the signature.


## -struct-fields




### -field dwType

Specifies the key information type encapsulated in this structure. 


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEYINFO_TYPE_KEYNAME"></a><a id="crypt_xml_keyinfo_type_keyname"></a><dl>
<dt><b>CRYPT_XML_KEYINFO_TYPE_KEYNAME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The structure specifies a key name.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEYINFO_TYPE_KEYVALUE"></a><a id="crypt_xml_keyinfo_type_keyvalue"></a><dl>
<dt><b>CRYPT_XML_KEYINFO_TYPE_KEYVALUE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The structure specifies the key value.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEYINFO_TYPE_RETRIEVAL"></a><a id="crypt_xml_keyinfo_type_retrieval"></a><dl>
<dt><b>CRYPT_XML_KEYINFO_TYPE_RETRIEVAL</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The structure specifies an XML encoded element that contains the key retrieval method.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEYINFO_TYPE_X509DATA"></a><a id="crypt_xml_keyinfo_type_x509data"></a><dl>
<dt><b>CRYPT_XML_KEYINFO_TYPE_X509DATA</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The structure specifies <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> data that  contains the key information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_KEYINFO_TYPE_CUSTOM"></a><a id="crypt_xml_keyinfo_type_custom"></a><dl>
<dt><b>CRYPT_XML_KEYINFO_TYPE_CUSTOM</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
The structure specifies user defined  information about the key information.

</td>
</tr>
</table>
 


### -field wszKeyName

A pointer to a null-terminated wide character string that contains the name of the key to retrieve.


### -field KeyValue

A <a href="https://msdn.microsoft.com/7aadd268-41bc-4ba3-babb-2ca7b13f378b">CRYPT_XML_KEY_VALUE</a> structure that contains the key value.


### -field RetrievalMethod

A <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure that contains XML encoded information about the key retrieval method.


### -field X509Data

A <a href="https://msdn.microsoft.com/4895a6e6-ffac-419f-af9b-f2062a1aecd4">CRYPT_XML_X509DATA</a> structure that contains X.509 data that contains the key.


### -field Custom

A <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure that contains user defined key information.

