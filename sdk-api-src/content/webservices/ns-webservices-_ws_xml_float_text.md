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

# _WS_XML_FLOAT_TEXT structure


## -description



        Represents a 4 byte floating point value.  (e.g. The value 0.0 represents the text "0")
      


## -struct-fields




### -field text


          The base type for all types that derive from <a href="https://msdn.microsoft.com/430edd13-b664-4e10-8d61-ffa6a01dcb90">WS_XML_TEXT</a>.
        


### -field value

The value.


## -remarks




        The textual representation of the value has enough digits to preserve the floating point value.
      


        Negative zero is represented by the text "-0".
      


        Positive infinity is represented by the text "INF";
      


        Negative infinity is represented by the text "-INF";
      


        Unrepresentable values are represented by the text "NaN".
      


        For more information on this representation, refer to IEEE Standard for Binary Floating-Point Arithmetic, available on the Web site http://www.ieee.org/.
      



