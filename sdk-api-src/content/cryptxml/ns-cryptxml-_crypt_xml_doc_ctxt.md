---
UID: NS:cryptxml._CRYPT_XML_DOC_CTXT
title: "_CRYPT_XML_DOC_CTXT"
author: windows-sdk-content
description: Defines document context information.
old-location: security\crypt_xml_doc_ctxt.htm
old-project: SecCrypto
ms.assetid: b57cccb1-b26f-4710-b888-f864cc9ae3be
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*PCRYPT_XML_DOC_CTXT, CRYPT_XML_DOC_CTXT, CRYPT_XML_DOC_CTXT structure [Security], PCRYPT_XML_DOC_CTXT, PCRYPT_XML_DOC_CTXT structure pointer [Security], _CRYPT_XML_DOC_CTXT, cryptxml/CRYPT_XML_DOC_CTXT, cryptxml/PCRYPT_XML_DOC_CTXT, security.crypt_xml_doc_ctxt"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CRYPT_XML_DOC_CTXT, *PCRYPT_XML_DOC_CTXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_DOC_CTXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_XML_DOC_CTXT structure


## -description


The <b>CRYPT_XML_DOC_CTXT</b> structure defines document context information.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hDocCtxt

The handle of the document context.


### -field pTransformsConfig

A pointer to a <a href="https://msdn.microsoft.com/ad18ee99-685d-4a79-bd91-492df20edb8c">CRYPT_XML_TRANSFORM_CHAIN_CONFIG</a> structure that contains information about the transform chain engine.


### -field cSignature

The number of elements in the array pointed to by the <b>rgpSignature</b> member.


### -field rgpSignature

A pointer to an array of <a href="https://msdn.microsoft.com/d9930946-aec0-42a4-949f-af8b2e9c6e6c">CRYPT_XML_SIGNATURE</a> structures that contain XML signature information.

