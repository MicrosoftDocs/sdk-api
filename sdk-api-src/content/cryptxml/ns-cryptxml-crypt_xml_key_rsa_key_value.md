---
UID: NS:cryptxml._CRYPT_XML_KEY_RSA_KEY_VALUE
title: CRYPT_XML_KEY_RSA_KEY_VALUE (cryptxml.h)
description: Defines an RSA key value. The CRYPT_XML_KEY_RSA_KEY_VALUE structure is used as element of the key value union in the CRYPT_XML_KEY_VALUE structure.
helpviewer_keywords: ["CRYPT_XML_KEY_RSA_KEY_VALUE","CRYPT_XML_KEY_RSA_KEY_VALUE structure [Security]","cryptxml/CRYPT_XML_KEY_RSA_KEY_VALUE","security.crypt_xml_key_rsa_key_value"]
old-location: security\crypt_xml_key_rsa_key_value.htm
tech.root: security
ms.assetid: e2b1344d-c108-4255-bd50-06d742ed67a8
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_KEY_RSA_KEY_VALUE, CRYPT_XML_KEY_RSA_KEY_VALUE structure [Security], cryptxml/CRYPT_XML_KEY_RSA_KEY_VALUE, security.crypt_xml_key_rsa_key_value
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
req.typenames: CRYPT_XML_KEY_RSA_KEY_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_KEY_RSA_KEY_VALUE
 - cryptxml/_CRYPT_XML_KEY_RSA_KEY_VALUE
 - CRYPT_XML_KEY_RSA_KEY_VALUE
 - cryptxml/CRYPT_XML_KEY_RSA_KEY_VALUE
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
 - CRYPT_XML_KEY_RSA_KEY_VALUE
---

# CRYPT_XML_KEY_RSA_KEY_VALUE structure


## -description

The <b>CRYPT_XML_KEY_RSA_KEY_VALUE</b> structure defines an RSA key value.  The <b>CRYPT_XML_KEY_RSA_KEY_VALUE</b> structure is used as element of the key value union  in the <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_value">CRYPT_XML_KEY_VALUE</a> structure.

## -struct-fields

### -field Modulus

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_data_blob">CRYPT_XML_DATA_BLOB</a> structure that contains the <a href="/windows/desktop/SecGloss/p-gly">public key</a> modulus data.

### -field Exponent

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_data_blob">CRYPT_XML_DATA_BLOB</a> structure that contains the public key exponent data.