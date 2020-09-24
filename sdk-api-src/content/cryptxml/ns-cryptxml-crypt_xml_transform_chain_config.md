---
UID: NS:cryptxml._CRYPT_XML_TRANSFORM_CHAIN_CONFIG
title: CRYPT_XML_TRANSFORM_CHAIN_CONFIG (cryptxml.h)
description: Contains application defined transforms that are allowed for use in the XML digital signature.
helpviewer_keywords: ["*PCRYPT_XML_TRANSFORM_CHAIN_CONFIG","CRYPT_XML_TRANSFORM_CHAIN_CONFIG","CRYPT_XML_TRANSFORM_CHAIN_CONFIG structure [Security]","PCRYPT_XML_TRANSFORM_CHAIN_CONFIG","PCRYPT_XML_TRANSFORM_CHAIN_CONFIG structure pointer [Security]","cryptxml/CRYPT_XML_TRANSFORM_CHAIN_CONFIG","cryptxml/PCRYPT_XML_TRANSFORM_CHAIN_CONFIG","security.crypt_xml_transform_chain_config"]
old-location: security\crypt_xml_transform_chain_config.htm
tech.root: security
ms.assetid: ad18ee99-685d-4a79-bd91-492df20edb8c
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_TRANSFORM_CHAIN_CONFIG, CRYPT_XML_TRANSFORM_CHAIN_CONFIG, CRYPT_XML_TRANSFORM_CHAIN_CONFIG structure [Security], PCRYPT_XML_TRANSFORM_CHAIN_CONFIG, PCRYPT_XML_TRANSFORM_CHAIN_CONFIG structure pointer [Security], cryptxml/CRYPT_XML_TRANSFORM_CHAIN_CONFIG, cryptxml/PCRYPT_XML_TRANSFORM_CHAIN_CONFIG, security.crypt_xml_transform_chain_config'
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
req.typenames: CRYPT_XML_TRANSFORM_CHAIN_CONFIG, *PCRYPT_XML_TRANSFORM_CHAIN_CONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_TRANSFORM_CHAIN_CONFIG
 - cryptxml/_CRYPT_XML_TRANSFORM_CHAIN_CONFIG
 - PCRYPT_XML_TRANSFORM_CHAIN_CONFIG
 - cryptxml/PCRYPT_XML_TRANSFORM_CHAIN_CONFIG
 - CRYPT_XML_TRANSFORM_CHAIN_CONFIG
 - cryptxml/CRYPT_XML_TRANSFORM_CHAIN_CONFIG
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
 - CRYPT_XML_TRANSFORM_CHAIN_CONFIG
---

# CRYPT_XML_TRANSFORM_CHAIN_CONFIG structure


## -description

The <b>CRYPT_XML_TRANSFORM_CHAIN_CONFIG</b> structure contains application defined transforms that are allowed for use  in the XML digital signature.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field cTransformInfo

The number of elements in the array pointed to by the <b>rgpTransformInfo</b> member.

### -field rgpTransformInfo

A pointer to an array of pointers to <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_transform_info">CRYPT_XML_TRANSFORM_INFO</a> structures that contain the transform parameters.