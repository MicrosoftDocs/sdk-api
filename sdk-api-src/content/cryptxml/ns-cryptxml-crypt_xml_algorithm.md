---
UID: NS:cryptxml._CRYPT_XML_ALGORITHM
title: CRYPT_XML_ALGORITHM (cryptxml.h)
description: Specifies the algorithm used to sign or transform the message.
helpviewer_keywords: ["*PCRYPT_XML_ALGORITHM","CRYPT_XML_ALGORITHM","CRYPT_XML_ALGORITHM structure [Security]","PCRYPT_XML_ALGORITHM","PCRYPT_XML_ALGORITHM structure pointer [Security]","cryptxml/CRYPT_XML_ALGORITHM","cryptxml/PCRYPT_XML_ALGORITHM","security.crypt_xml_algorithm"]
old-location: security\crypt_xml_algorithm.htm
tech.root: security
ms.assetid: 4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_ALGORITHM, CRYPT_XML_ALGORITHM, CRYPT_XML_ALGORITHM structure [Security], PCRYPT_XML_ALGORITHM, PCRYPT_XML_ALGORITHM structure pointer [Security], cryptxml/CRYPT_XML_ALGORITHM, cryptxml/PCRYPT_XML_ALGORITHM, security.crypt_xml_algorithm'
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
req.typenames: CRYPT_XML_ALGORITHM, *PCRYPT_XML_ALGORITHM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_ALGORITHM
 - cryptxml/_CRYPT_XML_ALGORITHM
 - PCRYPT_XML_ALGORITHM
 - cryptxml/PCRYPT_XML_ALGORITHM
 - CRYPT_XML_ALGORITHM
 - cryptxml/CRYPT_XML_ALGORITHM
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
 - CRYPT_XML_ALGORITHM
---

# CRYPT_XML_ALGORITHM structure


## -description

The <b>CRYPT_XML_ALGORITHM</b> structure specifies the algorithm used to sign or transform the message.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field wszAlgorithm

A pointer to a null-terminated Unicode string that contains the <b>Algorithm</b> attribute. 
    When the <b>Encoded</b> member contains an element that is proved by an application, this member is set to <b>NULL</b>.XML

### -field Encoded

Optional.  The XML encoded element. 
    This member  is set when an element tag is present in the XML signature.

## -see-also

<b></b>



<a href="/windows/desktop/SecCrypto/xml-digital-signature-cryptographic-algorithms">Digital Signature Cryptographic Algorithms</a>