---
UID: NS:cryptxml._CRYPT_XML_KEY_VALUE
title: CRYPT_XML_KEY_VALUE (cryptxml.h)
description: Contains a single public key that may be useful in validating the signature.
helpviewer_keywords: ["CRYPT_XML_KEY_VALUE","CRYPT_XML_KEY_VALUE structure [Security]","CRYPT_XML_KEY_VALUE_TYPE_CUSTOM","CRYPT_XML_KEY_VALUE_TYPE_DSA","CRYPT_XML_KEY_VALUE_TYPE_ECDSA","CRYPT_XML_KEY_VALUE_TYPE_RSA","cryptxml/CRYPT_XML_KEY_VALUE","security.crypt_xml_key_value"]
old-location: security\crypt_xml_key_value.htm
tech.root: security
ms.assetid: 7aadd268-41bc-4ba3-babb-2ca7b13f378b
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_KEY_VALUE, CRYPT_XML_KEY_VALUE structure [Security], CRYPT_XML_KEY_VALUE_TYPE_CUSTOM, CRYPT_XML_KEY_VALUE_TYPE_DSA, CRYPT_XML_KEY_VALUE_TYPE_ECDSA, CRYPT_XML_KEY_VALUE_TYPE_RSA, cryptxml/CRYPT_XML_KEY_VALUE, security.crypt_xml_key_value
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
req.typenames: CRYPT_XML_KEY_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_KEY_VALUE
 - cryptxml/_CRYPT_XML_KEY_VALUE
 - CRYPT_XML_KEY_VALUE
 - cryptxml/CRYPT_XML_KEY_VALUE
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
 - CRYPT_XML_KEY_VALUE
---

# CRYPT_XML_KEY_VALUE structure


## -description

The <b>CRYPT_XML_KEY_VALUE</b> structure contains a single <a href="/windows/desktop/SecGloss/p-gly">public key</a> that may be useful in validating the signature.

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
The key is an <a href="/windows/desktop/SecGloss/r-gly">RSA</a> key.

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

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_dsa_key_value">CRYPT_XML_KEY_DSA_KEY_VALUE</a> structure that contains <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) key data.

### -field RSAKeyValue

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_rsa_key_value">CRYPT_XML_KEY_RSA_KEY_VALUE</a> structure that contains RSA key data.

### -field ECDSAKeyValue

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_ecdsa_key_value">CRYPT_XML_KEY_ECDSA_KEY_VALUE</a> structure that contains ECDSA key data.

### -field Custom

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains custom key data.