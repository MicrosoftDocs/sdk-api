---
UID: NS:cryptxml._CRYPT_XML_DOC_CTXT
title: CRYPT_XML_DOC_CTXT (cryptxml.h)
description: Defines document context information.
helpviewer_keywords: ["*PCRYPT_XML_DOC_CTXT","CRYPT_XML_DOC_CTXT","CRYPT_XML_DOC_CTXT structure [Security]","PCRYPT_XML_DOC_CTXT","PCRYPT_XML_DOC_CTXT structure pointer [Security]","cryptxml/CRYPT_XML_DOC_CTXT","cryptxml/PCRYPT_XML_DOC_CTXT","security.crypt_xml_doc_ctxt"]
old-location: security\crypt_xml_doc_ctxt.htm
tech.root: security
ms.assetid: b57cccb1-b26f-4710-b888-f864cc9ae3be
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_DOC_CTXT, CRYPT_XML_DOC_CTXT, CRYPT_XML_DOC_CTXT structure [Security], PCRYPT_XML_DOC_CTXT, PCRYPT_XML_DOC_CTXT structure pointer [Security], cryptxml/CRYPT_XML_DOC_CTXT, cryptxml/PCRYPT_XML_DOC_CTXT, security.crypt_xml_doc_ctxt'
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
req.typenames: CRYPT_XML_DOC_CTXT, *PCRYPT_XML_DOC_CTXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_DOC_CTXT
 - cryptxml/_CRYPT_XML_DOC_CTXT
 - PCRYPT_XML_DOC_CTXT
 - cryptxml/PCRYPT_XML_DOC_CTXT
 - CRYPT_XML_DOC_CTXT
 - cryptxml/CRYPT_XML_DOC_CTXT
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
 - CRYPT_XML_DOC_CTXT
---

# CRYPT_XML_DOC_CTXT structure


## -description

The <b>CRYPT_XML_DOC_CTXT</b> structure defines document context information.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hDocCtxt

The handle of the document context.

### -field pTransformsConfig

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_transform_chain_config">CRYPT_XML_TRANSFORM_CHAIN_CONFIG</a> structure that contains information about the transform chain engine.

### -field cSignature

The number of elements in the array pointed to by the <b>rgpSignature</b> member.

### -field rgpSignature

A pointer to an array of <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_signature">CRYPT_XML_SIGNATURE</a> structures that contain XML signature information.