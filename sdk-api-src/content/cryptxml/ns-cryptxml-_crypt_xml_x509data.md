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

# _CRYPT_XML_X509DATA structure


## -description


The <b>CRYPT_XML_X509DATA</b> structure represents the sequence of choices in the <b>X509Data</b> element.


## -struct-fields




### -field cX509Data

The size, in bytes, of the buffer pointed to by the <b>rgX509Data</b> member.


### -field rgX509Data

A pointer to a <a href="https://msdn.microsoft.com/118371c7-9b75-4330-9897-bd352b072fa4">CRYPT_XML_X509DATA_ITEM</a> structure that contains data to encode.

