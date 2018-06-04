---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

