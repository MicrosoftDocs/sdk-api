---
UID: NS:cryptxml._CRYPT_XML_ISSUER_SERIAL
title: CRYPT_XML_ISSUER_SERIAL (cryptxml.h)
description: Contains an X.509 issued distinguished name—serial number pair.
helpviewer_keywords: ["CRYPT_XML_ISSUER_SERIAL","CRYPT_XML_ISSUER_SERIAL structure [Security]","cryptxml/CRYPT_XML_ISSUER_SERIAL","security.crypt_xml_issuer_serial"]
old-location: security\crypt_xml_issuer_serial.htm
tech.root: security
ms.assetid: 8d74e119-c7ea-4c7c-9d2a-e81f7ae40310
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_ISSUER_SERIAL, CRYPT_XML_ISSUER_SERIAL structure [Security], cryptxml/CRYPT_XML_ISSUER_SERIAL, security.crypt_xml_issuer_serial
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
req.typenames: CRYPT_XML_ISSUER_SERIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_ISSUER_SERIAL
 - cryptxml/_CRYPT_XML_ISSUER_SERIAL
 - CRYPT_XML_ISSUER_SERIAL
 - cryptxml/CRYPT_XML_ISSUER_SERIAL
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
 - CRYPT_XML_ISSUER_SERIAL
---

# CRYPT_XML_ISSUER_SERIAL structure


## -description

The <b>CRYPT_XML_ISSUER_SERIAL</b> structure contains an <a href="/windows/desktop/SecGloss/x-gly">X.509</a> issued distinguished name–serial number pair.

## -struct-fields

### -field wszIssuer

A pointer to a null-terminated wide character string that contains the issuer of the certificate.

### -field wszSerial

A pointer to a null-terminated wide character string that contains the serial number of the certificate.