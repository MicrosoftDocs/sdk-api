---
UID: NS:cryptxml._CRYPT_XML_SIGNATURE
title: CRYPT_XML_SIGNATURE (cryptxml.h)
description: Contains information used to populate the Signature element.
helpviewer_keywords: ["*PCRYPT_XML_SIGNATURE","CRYPT_XML_SIGNATURE","CRYPT_XML_SIGNATURE structure [Security]","PCRYPT_XML_SIGNATURE","PCRYPT_XML_SIGNATURE structure pointer [Security]","cryptxml/CRYPT_XML_SIGNATURE","cryptxml/PCRYPT_XML_SIGNATURE","security.crypt_xml_signature"]
old-location: security\crypt_xml_signature.htm
tech.root: security
ms.assetid: d9930946-aec0-42a4-949f-af8b2e9c6e6c
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_SIGNATURE, CRYPT_XML_SIGNATURE, CRYPT_XML_SIGNATURE structure [Security], PCRYPT_XML_SIGNATURE, PCRYPT_XML_SIGNATURE structure pointer [Security], cryptxml/CRYPT_XML_SIGNATURE, cryptxml/PCRYPT_XML_SIGNATURE, security.crypt_xml_signature'
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
req.typenames: CRYPT_XML_SIGNATURE, *PCRYPT_XML_SIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_SIGNATURE
 - cryptxml/_CRYPT_XML_SIGNATURE
 - PCRYPT_XML_SIGNATURE
 - cryptxml/PCRYPT_XML_SIGNATURE
 - CRYPT_XML_SIGNATURE
 - cryptxml/CRYPT_XML_SIGNATURE
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
 - CRYPT_XML_SIGNATURE
---

# CRYPT_XML_SIGNATURE structure


## -description

The <b>CRYPT_XML_SIGNATURE</b> structure contains information used to populate the <b>Signature</b> element.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hSignature

The handle of the signature to encode.

### -field wszId

A pointer to a null-terminated Unicode string that contains the value of the <b>Id</b> attribute.

### -field SignedInfo

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_signed_info">CRYPT_XML_SIGNED_INFO</a> structure that contains the canonicalization algorithm, 
    a signature algorithm, and one or more references. 
    The <b>SignedInfo</b> element can contain an optional ID attribute that will allow 
    the structure to be referenced by other signatures and objects.

### -field SignatureValue

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains a cryptographic signature value  used to populate the <b>Signature</b> element.

### -field pKeyInfo

Optional. A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_info">CRYPT_XML_KEY_INFO</a> structure that contains information that is encoded in the <b>KeyInfo</b> element.

### -field cObject

The number of  items in the array pointed to by the <b>rgpObject</b> member.

### -field rgpObject

Optional. A pointer to an array of  pointers to <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_object">CRYPT_XML_OBJECT</a> structures that  contain information that is encoded in <b>Object</b> elements.