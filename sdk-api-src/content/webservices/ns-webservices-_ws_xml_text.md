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

# _WS_XML_TEXT structure


## -description



        Represents a node of text content in xml.
      


## -struct-fields




### -field textType


## -remarks




        XML has no concept of typed content; all content is textual in nature.  In some cases this is inefficient, requiring
        translation between text and natural form (e.g. the characters '1','2','8' and the numerical value 128) or requiring
        more bytes of storage for the representation (e.g. the characters '2',5','5' might take 3 bytes, while the numerical
        value 255 could only take 1).
        This structure provides a way to indicate textual content in xml without physically representing it as the characters
        that comprise that value.
      



