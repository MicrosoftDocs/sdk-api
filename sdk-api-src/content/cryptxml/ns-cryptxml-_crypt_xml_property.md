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

# _CRYPT_XML_PROPERTY structure


## -description


The <b>CRYPT_XML_PROPERTY</b> structure contains information about a CryptXML property.


## -struct-fields




### -field dwPropId

A value of the <a href="https://msdn.microsoft.com/7b396245-6dc5-4018-821e-a70db5f0d068">CRYPT_XML_PROPERTY_ID</a> enumeration that specifies the property type.


### -field pvValue

A pointer to a buffer that contains the property value.


### -field cbValue

The size, in bytes, of the property value buffer pointed to by the <b>pvValue</b> member.

