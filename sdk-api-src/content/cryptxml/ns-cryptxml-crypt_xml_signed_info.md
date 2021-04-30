---
UID: NS:cryptxml._CRYPT_XML_SIGNED_INFO
title: CRYPT_XML_SIGNED_INFO (cryptxml.h)
description: Describes an XML encoded SignedInfo element.
helpviewer_keywords: ["*PCRYPT_XML_SIGNED_INFO","CRYPT_XML_SIGNED_INFO","CRYPT_XML_SIGNED_INFO structure [Security]","PCRYPT_XML_SIGNED_INFO","PCRYPT_XML_SIGNED_INFO structure pointer [Security]","cryptxml/CRYPT_XML_SIGNED_INFO","cryptxml/PCRYPT_XML_SIGNED_INFO","security.crypt_xml_signed_info"]
old-location: security\crypt_xml_signed_info.htm
tech.root: security
ms.assetid: 34f7f3be-8bf8-4863-9c94-79ee14a7ebea
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_SIGNED_INFO, CRYPT_XML_SIGNED_INFO, CRYPT_XML_SIGNED_INFO structure [Security], PCRYPT_XML_SIGNED_INFO, PCRYPT_XML_SIGNED_INFO structure pointer [Security], cryptxml/CRYPT_XML_SIGNED_INFO, cryptxml/PCRYPT_XML_SIGNED_INFO, security.crypt_xml_signed_info'
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
req.typenames: CRYPT_XML_SIGNED_INFO, *PCRYPT_XML_SIGNED_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_SIGNED_INFO
 - cryptxml/_CRYPT_XML_SIGNED_INFO
 - PCRYPT_XML_SIGNED_INFO
 - cryptxml/PCRYPT_XML_SIGNED_INFO
 - CRYPT_XML_SIGNED_INFO
 - cryptxml/CRYPT_XML_SIGNED_INFO
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
 - CRYPT_XML_SIGNED_INFO
---

# CRYPT_XML_SIGNED_INFO structure


## -description

The <b>CRYPT_XML_SIGNED_INFO</b> structure describes an XML encoded <b>SignedInfo</b> element.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field wszId

Optional.  A pointer to a null-terminated Unicode string that contains the <b>Id</b> attribute.

### -field Canonicalization

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the canonicalization algorithm.

### -field SignatureMethod

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the signature algorithm.

### -field cReference

The number of elements in the array pointed to by the <b>rgpReference</b> member.

### -field rgpReference

A pointer to an array of pointers to <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_reference">CRYPT_XML_REFERENCE</a> structures   that contain information that is encoded in <b>Reference</b> elements.

### -field Encoded

A  <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains the XML encoded <b>SignedInfo</b> element.