---
UID: NS:cryptxml._CRYPT_XML_DATA_PROVIDER
title: CRYPT_XML_DATA_PROVIDER (cryptxml.h)
description: Specifies the interface to the XML data provider.
helpviewer_keywords: ["*PCRYPT_XML_DATA_PROVIDER","CRYPT_XML_DATA_PROVIDER","CRYPT_XML_DATA_PROVIDER structure [Security]","PCRYPT_XML_DATA_PROVIDER","PCRYPT_XML_DATA_PROVIDER structure pointer [Security]","cryptxml/CRYPT_XML_DATA_PROVIDER","cryptxml/PCRYPT_XML_DATA_PROVIDER","security.crypt_xml_data_provider"]
old-location: security\crypt_xml_data_provider.htm
tech.root: security
ms.assetid: 98f32310-a4fa-414c-8a3e-877839eacd1b
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_DATA_PROVIDER, CRYPT_XML_DATA_PROVIDER, CRYPT_XML_DATA_PROVIDER structure [Security], PCRYPT_XML_DATA_PROVIDER, PCRYPT_XML_DATA_PROVIDER structure pointer [Security], cryptxml/CRYPT_XML_DATA_PROVIDER, cryptxml/PCRYPT_XML_DATA_PROVIDER, security.crypt_xml_data_provider'
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
req.typenames: CRYPT_XML_DATA_PROVIDER, *PCRYPT_XML_DATA_PROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_DATA_PROVIDER
 - cryptxml/_CRYPT_XML_DATA_PROVIDER
 - PCRYPT_XML_DATA_PROVIDER
 - cryptxml/PCRYPT_XML_DATA_PROVIDER
 - CRYPT_XML_DATA_PROVIDER
 - cryptxml/CRYPT_XML_DATA_PROVIDER
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
 - CRYPT_XML_DATA_PROVIDER
---

# CRYPT_XML_DATA_PROVIDER structure


## -description

The <b>CRYPT_XML_DATA_PROVIDER</b> structure specifies the interface to the XML data provider.

## -struct-fields

### -field pvCallbackState

An application-defined argument that is passed to
    the <b>pfnRead</b> and <b>pfnClose</b> callback functions.

### -field cbBufferSize

 The size, in bytes, of the data provider's buffer. The size can be zero if the size does not matter or if the size cannot be determined by the provider.
    This value is used by a caller of <b>pfnRead</b> to determine the necessary size of the receiving buffer.

### -field pfnRead

A pointer to a <a href="/windows/desktop/api/cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read">PFN_CRYPT_XML_DATA_PROVIDER_READ</a> callback function used to read data.

### -field pfnClose

A pointer to a <a href="/windows/desktop/api/cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close">PFN_CRYPT_XML_DATA_PROVIDER_CLOSE</a> callback function used to release the data provider. When you have finished using the data provider, you must release it.