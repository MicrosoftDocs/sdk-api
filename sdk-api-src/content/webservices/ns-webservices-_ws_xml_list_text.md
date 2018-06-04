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

# _WS_XML_LIST_TEXT structure


## -description



        Represents a list of text values separated by a single whitespace character.
      


        (e.g. The list { { WS_XML_TEXT_TYPE_INT32 }, 123}, 
        { { WS_XML_TEXT_TYPE_BOOL }, 1 } represents the text "123 true")
      


## -struct-fields




### -field text


          The base type for all types that derive from <a href="https://msdn.microsoft.com/430edd13-b664-4e10-8d61-ffa6a01dcb90">WS_XML_TEXT</a>.
        


### -field itemCount


          The number of items in the list.
        


### -field items


          The list of items.
        

