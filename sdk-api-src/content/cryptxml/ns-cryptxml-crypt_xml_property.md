---
UID: NS:cryptxml._CRYPT_XML_PROPERTY
title: CRYPT_XML_PROPERTY (cryptxml.h)
author: windows-sdk-content
description: Contains information about a CryptXML property.
old-location: security\crypt_xml_property.htm
tech.root: SecCrypto
ms.assetid: 287c205a-56ba-40ae-a664-9bccef2e9655
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRYPT_XML_PROPERTY, CRYPT_XML_PROPERTY, CRYPT_XML_PROPERTY structure [Security], PCRYPT_XML_PROPERTY, PCRYPT_XML_PROPERTY structure pointer [Security], cryptxml/CRYPT_XML_PROPERTY, cryptxml/PCRYPT_XML_PROPERTY, security.crypt_xml_property"
ms.topic: struct
f1_keywords: 
 - "cryptxml/CRYPT_XML_PROPERTY"
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
 - CRYPT_XML_PROPERTY
targetos: Windows
req.typenames: CRYPT_XML_PROPERTY, *PCRYPT_XML_PROPERTY
req.redist: 
ms.custom: 19H1
---

# CRYPT_XML_PROPERTY structure


## -description


The <b>CRYPT_XML_PROPERTY</b> structure contains information about a CryptXML property.


## -struct-fields




### -field dwPropId

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/ne-cryptxml-crypt_xml_property_id">CRYPT_XML_PROPERTY_ID</a> enumeration that specifies the property type.


### -field pvValue

A pointer to a buffer that contains the property value.


### -field cbValue

The size, in bytes, of the property value buffer pointed to by the <b>pvValue</b> member.

