---
UID: NS:cryptxml._CRYPT_XML_X509DATA
title: CRYPT_XML_X509DATA (cryptxml.h)
description: Represents the sequence of choices in the X509Data element.
helpviewer_keywords: ["CRYPT_XML_X509DATA","CRYPT_XML_X509DATA structure [Security]","PCRYPT_XML_X509DATA","PCRYPT_XML_X509DATA structure pointer [Security]","cryptxml/CRYPT_XML_X509DATA","cryptxml/PCRYPT_XML_X509DATA","security.crypt_xml_x509data"]
old-location: security\crypt_xml_x509data.htm
tech.root: security
ms.assetid: 4895a6e6-ffac-419f-af9b-f2062a1aecd4
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_X509DATA, CRYPT_XML_X509DATA structure [Security], PCRYPT_XML_X509DATA, PCRYPT_XML_X509DATA structure pointer [Security], cryptxml/CRYPT_XML_X509DATA, cryptxml/PCRYPT_XML_X509DATA, security.crypt_xml_x509data
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
req.typenames: CRYPT_XML_X509DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_X509DATA
 - cryptxml/_CRYPT_XML_X509DATA
 - CRYPT_XML_X509DATA
 - cryptxml/CRYPT_XML_X509DATA
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
 - CRYPT_XML_X509DATA
---

# CRYPT_XML_X509DATA structure


## -description

The <b>CRYPT_XML_X509DATA</b> structure represents the sequence of choices in the <b>X509Data</b> element.

## -struct-fields

### -field cX509Data

The size, in bytes, of the buffer pointed to by the <b>rgX509Data</b> member.

### -field rgX509Data

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_x509data_item">CRYPT_XML_X509DATA_ITEM</a> structure that contains data to encode.