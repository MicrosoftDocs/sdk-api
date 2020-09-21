---
UID: NS:cryptxml._CRYPT_XML_KEY_INFO_ITEM
title: CRYPT_XML_KEY_INFO_ITEM (cryptxml.h)
description: Encapsulates key information data that corresponds to a KeyInfo element. The KeyInfo element enables the recipient to obtain the key needed to validate the signature.
helpviewer_keywords: ["CRYPT_XML_KEYINFO_TYPE_CUSTOM","CRYPT_XML_KEYINFO_TYPE_KEYNAME","CRYPT_XML_KEYINFO_TYPE_KEYVALUE","CRYPT_XML_KEYINFO_TYPE_RETRIEVAL","CRYPT_XML_KEYINFO_TYPE_X509DATA","CRYPT_XML_KEY_INFO_ITEM","CRYPT_XML_KEY_INFO_ITEM structure [Security]","cryptxml/CRYPT_XML_KEY_INFO_ITEM","security.crypt_xml_key_info_item"]
old-location: security\crypt_xml_key_info_item.htm
tech.root: security
ms.assetid: 3fbb1623-d493-49f1-a004-74ec8d22520e
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_KEYINFO_TYPE_CUSTOM, CRYPT_XML_KEYINFO_TYPE_KEYNAME, CRYPT_XML_KEYINFO_TYPE_KEYVALUE, CRYPT_XML_KEYINFO_TYPE_RETRIEVAL, CRYPT_XML_KEYINFO_TYPE_X509DATA, CRYPT_XML_KEY_INFO_ITEM, CRYPT_XML_KEY_INFO_ITEM structure [Security], cryptxml/CRYPT_XML_KEY_INFO_ITEM, security.crypt_xml_key_info_item
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
req.typenames: CRYPT_XML_KEY_INFO_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_KEY_INFO_ITEM
 - cryptxml/_CRYPT_XML_KEY_INFO_ITEM
 - CRYPT_XML_KEY_INFO_ITEM
 - cryptxml/CRYPT_XML_KEY_INFO_ITEM
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
 - CRYPT_XML_KEY_INFO_ITEM
---

# CRYPT_XML_KEY_INFO_ITEM structure


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
The structure specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> data that  contains the key information.

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

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_value">CRYPT_XML_KEY_VALUE</a> structure that contains the key value.

### -field RetrievalMethod

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains XML encoded information about the key retrieval method.

### -field X509Data

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_x509data">CRYPT_XML_X509DATA</a> structure that contains X.509 data that contains the key.

### -field Custom

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains user defined key information.