---
UID: NS:cryptxml._CRYPT_XML_KEY_ECDSA_KEY_VALUE
title: CRYPT_XML_KEY_ECDSA_KEY_VALUE (cryptxml.h)
author: windows-sdk-content
description: Defines an Elliptic Curve Digital Signature Algorithm (ECDSA) key value. The CRYPT_XML_KEY_ECDSA_KEY_VALUE structure is used as an element of the key value union in the CRYPT_XML_KEY_VALUE structure.
old-location: security\crypt_xml_key_ecdsa_key_value.htm
tech.root: SecCrypto
ms.assetid: db7e8ee0-25b4-4e2e-83da-f970906c9da9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_KEY_ECDSA_KEY_VALUE, CRYPT_XML_KEY_ECDSA_KEY_VALUE structure [Security], cryptxml/CRYPT_XML_KEY_ECDSA_KEY_VALUE, security.crypt_xml_key_ecdsa_key_value
ms.topic: struct
f1_keywords:
- cryptxml/CRYPT_XML_KEY_ECDSA_KEY_VALUE
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Cryptxml.h
api_name:
- CRYPT_XML_KEY_ECDSA_KEY_VALUE
targetos: Windows
req.typenames: CRYPT_XML_KEY_ECDSA_KEY_VALUE
req.redist: 
ms.custom: 19H1
---

# CRYPT_XML_KEY_ECDSA_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_ECDSA_KEY_VALUE</b> structure defines an Elliptic Curve Digital Signature Algorithm (ECDSA) key value.  The <b>CRYPT_XML_KEY_ECDSA_KEY_VALUE</b> structure is used as an element of the key value union  in the <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_value">CRYPT_XML_KEY_VALUE</a> structure.


## -struct-fields




### -field wszNamedCurve

A pointer to a null-terminated Unicode string that contains the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the named curve.


### -field X

Defines the X value of an ECDSA curve.


### -field Y

Defines the Y value of an ECDSA curve.


### -field ExplicitPara

A   <b>CRYPT_XML_BLOB</b> value that defines the encoded parameters of an ECDSA curve.

