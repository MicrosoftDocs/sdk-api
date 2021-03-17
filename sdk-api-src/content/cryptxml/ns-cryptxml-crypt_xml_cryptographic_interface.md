---
UID: NS:cryptxml._CRYPT_XML_CRYPTOGRAPHIC_INTERFACE
title: CRYPT_XML_CRYPTOGRAPHIC_INTERFACE (cryptxml.h)
description: Exposes the implemented CryptXML functions.
helpviewer_keywords: ["*PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE","*PCRYPT_XML_CRYPTO_PROVIDER","CRYPT_XML_CRYPTOGRAPHIC_INTERFACE","CRYPT_XML_CRYPTOGRAPHIC_INTERFACE structure [Security]","PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE","PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE structure pointer [Security]","cryptxml/CRYPT_XML_CRYPTOGRAPHIC_INTERFACE","cryptxml/PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE","security.crypt_xml_cryptographic_interface"]
old-location: security\crypt_xml_cryptographic_interface.htm
tech.root: security
ms.assetid: 55585a57-be3e-492d-bf56-4e2456572161
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE, *PCRYPT_XML_CRYPTO_PROVIDER, CRYPT_XML_CRYPTOGRAPHIC_INTERFACE, CRYPT_XML_CRYPTOGRAPHIC_INTERFACE structure [Security], PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE, PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE structure pointer [Security], cryptxml/CRYPT_XML_CRYPTOGRAPHIC_INTERFACE, cryptxml/PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE, security.crypt_xml_cryptographic_interface'
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
req.typenames: CRYPT_XML_CRYPTOGRAPHIC_INTERFACE, *PCRYPT_XML_CRYPTO_PROVIDER, *PCRYPT_XML_CRYPTOGRAPHIC_INTERFACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_CRYPTOGRAPHIC_INTERFACE
 - cryptxml/_CRYPT_XML_CRYPTOGRAPHIC_INTERFACE
 - PCRYPT_XML_CRYPTO_PROVIDER
 - cryptxml/PCRYPT_XML_CRYPTO_PROVIDER
 - CRYPT_XML_CRYPTOGRAPHIC_INTERFACE
 - cryptxml/CRYPT_XML_CRYPTOGRAPHIC_INTERFACE
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
 - CRYPT_XML_CRYPTOGRAPHIC_INTERFACE
---

# CRYPT_XML_CRYPTOGRAPHIC_INTERFACE structure


## -description

The <b>CRYPT_XML_CRYPTOGRAPHIC_INTERFACE</b> structure is passed to the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a> function pointer to expose the implemented CryptXML functions.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field fpCryptXmlEncodeAlgorithm

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm">CryptXmlDllEncodeAlgorithm</a> function.

### -field fpCryptXmlCreateDigest

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest">CryptXmlDllCreateDigest</a> function.

### -field fpCryptXmlDigestData

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata">CryptXmlDllDigestData</a> function.

### -field fpCryptXmlFinalizeDigest

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest">CryptXmlDllFinalizeDigest</a> function.

### -field fpCryptXmlCloseDigest

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest">CryptXmlDllCloseDigest</a> function.

### -field fpCryptXmlSignData

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllsigndata">CryptXmlDllSignData</a> function.

### -field fpCryptXmlVerifySignature

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature">CryptXmlDllVerifySignature</a> function.

### -field fpCryptXmlGetAlgorithmInfo

A pointer to the implementation of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo">CryptXmlDllGetAlgorithmInfo</a> function.