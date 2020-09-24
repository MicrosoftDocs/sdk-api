---
UID: NF:cryptxml.CryptXmlOpenToEncode
title: CryptXmlOpenToEncode function (cryptxml.h)
description: Opens an XML digital signature to encode and returns a handle of the opened Signature element. The handle encapsulates a document context with a single CRYPT_XML_SIGNATURE structure and remains open until the CryptXmlClose function is called.
helpviewer_keywords: ["CRYPT_XML_FLAG_DISABLE_EXTENSIONS","CRYPT_XML_FLAG_NO_SERIALIZE","CryptXmlOpenToEncode","CryptXmlOpenToEncode function [Security]","cryptxml/CryptXmlOpenToEncode","security.cryptxmlopentoencode"]
old-location: security\cryptxmlopentoencode.htm
tech.root: security
ms.assetid: a313d14c-03fc-4719-bacd-c7b3e5ce2dba
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_FLAG_DISABLE_EXTENSIONS, CRYPT_XML_FLAG_NO_SERIALIZE, CryptXmlOpenToEncode, CryptXmlOpenToEncode function [Security], cryptxml/CryptXmlOpenToEncode, security.cryptxmlopentoencode
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
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlOpenToEncode
 - cryptxml/CryptXmlOpenToEncode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlOpenToEncode
---

# CryptXmlOpenToEncode function


## -description

If <b>CryptXmlOpenToEncode</b> function opens an XML digital signature to encode and returns a handle of the opened <b>Signature</b> element. The handle encapsulates a document context with a single <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_signature">CRYPT_XML_SIGNATURE</a> structure and remains open until the <a href="/windows/desktop/api/cryptxml/nf-cryptxml-cryptxmlclose">CryptXmlClose</a> function is called.

## -parameters

### -param pConfig [in, optional]

The handle of the transform chain engine. If this parameter is <b>NULL</b>, then a default engine is used to apply transforms.

### -param dwFlags

A <b>DWORD</b> value that controls which CryptXML extensions are loaded and whether the XML is serialized. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_NO_SERIALIZE"></a><a id="crypt_xml_flag_no_serialize"></a><dl>
<dt><b>CRYPT_XML_FLAG_NO_SERIALIZE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Inhibit serialization.


<div class="alert"><b>Note</b>  Do not set this flag when multiple threads are accessing a CryptXml object. Serialization ensures mutual exclusion when two or more threads attempt 
to simultaneously accept a CryptXml object or memory.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_DISABLE_EXTENSIONS"></a><a id="crypt_xml_flag_disable_extensions"></a><dl>
<dt><b>CRYPT_XML_FLAG_DISABLE_EXTENSIONS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Only default implementations for the signature and digest are used. When this flag is set, no other registered extensions are loaded.

</td>
</tr>
</table>

### -param wszId [in, optional]

A pointer to a null-terminated Unicode string that contains the <b>Id</b> attribute of the <b>Signature</b> element.
If this parameter is <b>NULL</b>, then a new GUID is generated. If this parameter is an empty string, then no <b>Id</b> attribute is produced.

### -param rgProperty [in]

A pointer to an array of <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_property">CRYPT_XML_PROPERTY</a> structures that specify additional properties.

### -param cProperty [in]

The number of elements in the array pointed to by the <i>rgProperty</i> parameter.

### -param pEncoded [in, optional]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains the signature to encode.

### -param phSignature [optional]

The handle to the <b>Signature</b> element.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.