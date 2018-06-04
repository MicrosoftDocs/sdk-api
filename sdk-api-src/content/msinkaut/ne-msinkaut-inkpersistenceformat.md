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

# InkPersistenceFormat enumeration


## -description



Specifies how ink is persisted.




## -enum-fields




### -field IPF_InkSerializedFormat

Ink is persisted using ink serialized format (ISF).

This is the most compact persistent representation of ink. It can be embedded within a binary document format or placed directly on the Clipboard.


### -field IPF_Base64InkSerializedFormat

Ink is persisted by encoding the ISF as a base64 stream.

This format is provided so that ink can be encoded directly in an Extensible Markup Language (XML) or HTML file.


### -field IPF_GIF


### -field IPF_Base64GIF




#### - IPF_Base64Gif

Ink is persisted by using a base64 encoded fortified.

This GIF format is provided when ink is to be encoded directly in an XML or HTML file with later conversion into an image. A possible use of this would be in an XML format that is generated to contain all ink information and used as a way to generate HTML through Extensible Stylesheet Language Transformations (XSLT).


#### - IPF_Gif

Ink is persisted by using a Graphics Interchange Format (GIF) file that contains ISF as metadata that is embedded within the file.

This allows ink to be viewed in applications that are not ink-enabled and maintain its full ink fidelity when it returns to an ink-enabled application. This format is ideal when transporting ink content within an HTML file and making it usable by ink-enabled and ink-unaware applications.


## -see-also




<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/31da19a7-207f-4f11-9b0f-7402e9727f59">Save Method [InkDisp Class]</a>
 

 

