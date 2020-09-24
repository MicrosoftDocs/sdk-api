---
UID: NS:cryptxml._CRYPT_XML_REFERENCE
title: CRYPT_XML_REFERENCE (cryptxml.h)
description: Contains information used to populate the Reference element.
helpviewer_keywords: ["*PCRYPT_XML_REFERENCE","CRYPT_XML_REFERENCE","CRYPT_XML_REFERENCE structure [Security]","PCRYPT_XML_REFERENCE","PCRYPT_XML_REFERENCE structure pointer [Security]","cryptxml/CRYPT_XML_REFERENCE","cryptxml/PCRYPT_XML_REFERENCE","security.crypt_xml_reference"]
old-location: security\crypt_xml_reference.htm
tech.root: security
ms.assetid: af16af5a-b1e5-4250-bdb1-f3fceb1830b9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_REFERENCE, CRYPT_XML_REFERENCE, CRYPT_XML_REFERENCE structure [Security], PCRYPT_XML_REFERENCE, PCRYPT_XML_REFERENCE structure pointer [Security], cryptxml/CRYPT_XML_REFERENCE, cryptxml/PCRYPT_XML_REFERENCE, security.crypt_xml_reference'
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
req.typenames: CRYPT_XML_REFERENCE, *PCRYPT_XML_REFERENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_REFERENCE
 - cryptxml/_CRYPT_XML_REFERENCE
 - PCRYPT_XML_REFERENCE
 - cryptxml/PCRYPT_XML_REFERENCE
 - CRYPT_XML_REFERENCE
 - cryptxml/CRYPT_XML_REFERENCE
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
 - CRYPT_XML_REFERENCE
---

# CRYPT_XML_REFERENCE structure


## -description

The <b>CRYPT_XML_REFERENCE</b> structure contains information used to populate the <b>Reference</b> element.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hReference

The handle of the <b>Reference</b> element.

### -field wszId

Optional. A pointer to a null-terminated Unicode string that contains the value of the <b>Id</b> attribute.

### -field wszUri

 A pointer to a null-terminated Unicode string that contains a <b>URI</b> attribute.

### -field wszType

A pointer to a null-terminated Unicode string that contains the value of the <b>Type</b> attribute.

### -field DigestMethod

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the digest method.

### -field DigestValue

A <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DATA_BLOB</a> structure that specifies the hash value.

### -field cTransform

The number of elements in the array pointed to by the <b>rgTransform</b> member.

### -field rgTransform

An array of <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_transform_info">CRYPT_XML_TRANSFORM_INFO</a> structures  that contain information about the transform applied to the signed data.