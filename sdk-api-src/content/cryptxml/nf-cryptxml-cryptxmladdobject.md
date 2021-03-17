---
UID: NF:cryptxml.CryptXmlAddObject
title: CryptXmlAddObject function (cryptxml.h)
description: Adds the Object element to the Signature in the Document Context opened for encoding.
helpviewer_keywords: ["CRYPT_XML_ADD_OBJECT_CREATE_REFERENCE","CryptXmlAddObject","CryptXmlAddObject function [Security]","cryptxml/CryptXmlAddObject","security.cryptxmladdobject"]
old-location: security\cryptxmladdobject.htm
tech.root: security
ms.assetid: 906c17a2-d8f3-4f90-a697-432cae7c789a
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_ADD_OBJECT_CREATE_REFERENCE, CryptXmlAddObject, CryptXmlAddObject function [Security], cryptxml/CryptXmlAddObject, security.cryptxmladdobject
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
 - CryptXmlAddObject
 - cryptxml/CryptXmlAddObject
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
 - CryptXmlAddObject
---

# CryptXmlAddObject function


## -description

The <b>CryptXmlAddObject</b> function adds the <b>Object</b> element to the Signature in the Document Context opened for encoding.

## -parameters

### -param hSignatureOrObject [in]

The handle of a Signature returned by the <a href="/windows/desktop/api/cryptxml/nf-cryptxml-cryptxmlopentoencode">CryptXmlOpenToEncode</a> function or the handle of a Reference returned by the <a href="/windows/desktop/api/cryptxml/nf-cryptxml-cryptxmlcreatereference">CryptXmlCreateReference</a> function with     the <b>CRYPT_XML_FLAG_CREATE_REFERENCE_AS_OBJECT</b> flag set.

### -param dwFlags

Specifies flags that control the manner in which the object is added.


Currently defined <i>dwFlags</i> values are shown in the following table .



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_ADD_OBJECT_CREATE_REFERENCE"></a><a id="crypt_xml_add_object_create_reference"></a><dl>
<dt><b>CRYPT_XML_ADD_OBJECT_CREATE_REFERENCE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
When set, an in-memory copy of the XML part is created and included in the <b>Object</b> element.

</td>
</tr>
</table>

### -param rgProperty [in, optional]

A pointer to  a  <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_property">CRYPT_XML_PROPERTY</a> structure that specifies additional properties used to decode the <b>Object</b> element.

### -param cProperty [in]

The number of elements in the array pointed to by the <i>rgProperty</i> property.

### -param pEncoded [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains the <b>Object</b> element.

### -param ppObject [out, optional]

A pointer to  a pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_object">CRYPT_XML_OBJECT</a> structure to receive the decoded structure.
    This parameter must be <b>NULL</b> when the <i>hSignatureOrObject</i> parameter contains a handle to the Object.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

## -remarks

    When the <i>hSignatureOrObject</i> parameter specifies a handle to a Reference returned 
    by the <a href="/windows/desktop/api/cryptxml/nf-cryptxml-cryptxmlcreatereference">CryptXmlCreateReference</a> function, the <i>pEncoded</i> parameter specifies XML content that is included
    in the <b>Object</b> node after the optional <b>Manifest</b> element.
    The pointer contained in the <i>pEncoded</i>  parameter must be valid until the signature is complete. 
    Otherwise, use the <b>CRYPT_XML_FLAG_ADD_OBJECT_CREATE_COPY</b> flag to create an in-memory copy.