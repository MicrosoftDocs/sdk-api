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

# _WS_XML_STRING structure


## -description



        Represents a string that optionally has <a href="https://msdn.microsoft.com/2cba47fd-a049-4e50-99dd-20ccf91c9e0f">dictionary</a> 
        information associated with it.  The xml APIs use WS_XML_STRINGs to identify prefixes, 
        localNames and namespaces.
      


## -struct-fields




### -field length


          The number of bytes in the UTF-8 encoded representation of the string.
        


### -field bytes


          The string encoded as UTF-8 bytes.
        


### -field dictionary


          A pointer to the dictionary that contains the string.  If the string is not part of a dictionary
          then the value may be <b>NULL</b>.
        


### -field id


          A value that uniquely identifies the string within the specified dictionary.
          The entry at dictionary-&gt;strings[id] should identify this string.
        


          If the dictionary is <b>NULL</b>, then this value is unused.
        


## -remarks




        The string is represented as UTF-8 encoded bytes, not WCHARs.  It is not required to be zero terminated.
      


        The macros <a href="https://msdn.microsoft.com/95e2326c-d4b2-421c-b991-ca9c332b6f6f">WS_XML_STRING_VALUE</a>, <a href="https://msdn.microsoft.com/3a5abf34-16f6-4cac-a5da-35045de4438b">WS_XML_STRING_NULL</a>  and
        <a href="https://msdn.microsoft.com/1e2045c0-11c5-4369-9b82-dc759eb1412e">WS_XML_STRING_DICTIONARY_VALUE</a> can be used to initialize this structure.
      


        The dictionary information is used by the binary encoding to write a more compact xml document.
      



