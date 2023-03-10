---
UID: NS:cryptxml._CRYPT_XML_DATA_BLOB
title: CRYPT_XML_DATA_BLOB (cryptxml.h)
description: Contains XML encoded data.
helpviewer_keywords: ["*PCRYPT_XML_DATA_BLOB","CRYPT_XML_DATA_BLOB","CRYPT_XML_DATA_BLOB structure [Security]","PCRYPT_XML_DATA_BLOB","PCRYPT_XML_DATA_BLOB structure pointer [Security]","cryptxml/CRYPT_XML_DATA_BLOB","cryptxml/PCRYPT_XML_DATA_BLOB","security.crypt_xml_data_blob"]
old-location: security\crypt_xml_data_blob.htm
tech.root: security
ms.assetid: dc7e23d6-923c-40d2-9cf7-9a529c0634ce
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_DATA_BLOB, CRYPT_XML_DATA_BLOB, CRYPT_XML_DATA_BLOB structure [Security], PCRYPT_XML_DATA_BLOB, PCRYPT_XML_DATA_BLOB structure pointer [Security], cryptxml/CRYPT_XML_DATA_BLOB, cryptxml/PCRYPT_XML_DATA_BLOB, security.crypt_xml_data_blob'
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
req.typenames: CRYPT_XML_DATA_BLOB, *PCRYPT_XML_DATA_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_DATA_BLOB
 - cryptxml/_CRYPT_XML_DATA_BLOB
 - PCRYPT_XML_DATA_BLOB
 - cryptxml/PCRYPT_XML_DATA_BLOB
 - CRYPT_XML_DATA_BLOB
 - cryptxml/CRYPT_XML_DATA_BLOB
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
 - CRYPT_XML_DATA_BLOB
---

# CRYPT_XML_DATA_BLOB structure


## -description

The <b>CRYPT_XML_DATA_BLOB</b> structure contains XML encoded data.

## -struct-fields

### -field cbData

The size, in bytes, of the data buffer pointed to by the <b>pbData</b> member.

### -field pbData

A pointer to the XML data. The maximum length in the buffer cannot exceed <b>CRYPT_XML_BLOB_MAX</b>              bytes.

