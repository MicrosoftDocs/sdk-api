---
UID: NS:cryptxml._CRYPT_XML_PROPERTY
title: CRYPT_XML_PROPERTY (cryptxml.h)
description: Contains information about a CryptXML property.
helpviewer_keywords: ["*PCRYPT_XML_PROPERTY","CRYPT_XML_PROPERTY","CRYPT_XML_PROPERTY structure [Security]","PCRYPT_XML_PROPERTY","PCRYPT_XML_PROPERTY structure pointer [Security]","cryptxml/CRYPT_XML_PROPERTY","cryptxml/PCRYPT_XML_PROPERTY","security.crypt_xml_property"]
old-location: security\crypt_xml_property.htm
tech.root: security
ms.assetid: 287c205a-56ba-40ae-a664-9bccef2e9655
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_PROPERTY, CRYPT_XML_PROPERTY, CRYPT_XML_PROPERTY structure [Security], PCRYPT_XML_PROPERTY, PCRYPT_XML_PROPERTY structure pointer [Security], cryptxml/CRYPT_XML_PROPERTY, cryptxml/PCRYPT_XML_PROPERTY, security.crypt_xml_property'
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
req.typenames: CRYPT_XML_PROPERTY, *PCRYPT_XML_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_PROPERTY
 - cryptxml/_CRYPT_XML_PROPERTY
 - PCRYPT_XML_PROPERTY
 - cryptxml/PCRYPT_XML_PROPERTY
 - CRYPT_XML_PROPERTY
 - cryptxml/CRYPT_XML_PROPERTY
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
 - CRYPT_XML_PROPERTY
---

# CRYPT_XML_PROPERTY structure


## -description

The <b>CRYPT_XML_PROPERTY</b> structure contains information about a CryptXML property.

## -struct-fields

### -field dwPropId

A value of the <a href="/windows/desktop/api/cryptxml/ne-cryptxml-crypt_xml_property_id">CRYPT_XML_PROPERTY_ID</a> enumeration that specifies the property type.

### -field pvValue

A pointer to a buffer that contains the property value.

### -field cbValue

The size, in bytes, of the property value buffer pointed to by the <b>pvValue</b> member.