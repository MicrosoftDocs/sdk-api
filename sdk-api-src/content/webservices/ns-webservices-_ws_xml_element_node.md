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

# _WS_XML_ELEMENT_NODE structure


## -description



        Represents a start element in xml (e.g. 
        &lt;a:purchaseOrder xmlns:a="http://tempuri.org" id="5"&gt;)
      


## -struct-fields




### -field node


          The base type for all types that derive from <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">WS_XML_NODE</a>.
        


### -field prefix


          The prefix of the element.  In the example, it refers to "a".  Empty prefixes are represented by a zero length <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a>.
        


### -field localName


          The localName of the element.  In the example, it refers to "purchaseOrder".
        


### -field ns


          The resolved namespace of the prefix.  In the example, it refers to "http://tempuri.org".
        


### -field attributeCount


          The number of attributes on the element.  In the example, it would be 2.
        


### -field attributes


          The array of attributes for the element.
        


### -field isEmpty


          Whether the element is an empty element or not.  In the example, it would be <b>FALSE</b>.
        

