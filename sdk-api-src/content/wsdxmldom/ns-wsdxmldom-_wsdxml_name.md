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

# _WSDXML_NAME structure


## -description


Specifies an XML qualified name.


## -struct-fields




### -field Space

Reference to a <a href="https://msdn.microsoft.com/dcf27f38-e628-4b0c-859c-ad12d3ed0924">WSDXML_NAMESPACE</a> structure that specifies the namespace of the qualified name.


### -field LocalName

The local name of the qualified name.


## -remarks



<b>WSDXML_NAME</b> represents a single name within a namespace. The relationship between the name and namespace is circular, in that the <b>Space</b> pointer of the name points to the namespace the name belongs to, and the <b>Names</b> array of the namespace will have an entry for the name.



