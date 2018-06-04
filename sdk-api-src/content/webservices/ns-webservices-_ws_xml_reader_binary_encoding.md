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

# _WS_XML_READER_BINARY_ENCODING structure


## -description



        Used to indicate that the reader should interpret the bytes it reads as binary xml.
      


## -struct-fields




### -field encoding


          The base type for all types that derive from <a href="https://msdn.microsoft.com/54d9683e-c2d1-4e18-92a2-a68558999e28">WS_XML_READER_ENCODING</a>.
        


### -field staticDictionary


          Indicates the dictionary that the reader should use for static strings.  The binary representation of the xml
          document references these strings by id (as opposed to embedding the actual string), and therefore they must contain 
          the same set of strings used when the document was written.
        


### -field dynamicDictionary


          Indicates the dictionary that the reader should use for dynamic strings. These are strings that were not in the 
          staticDictionary when the document was written but that were found by the <a href="https://msdn.microsoft.com/c1520c9a-4360-4ac0-89b8-e80385668051">WS_DYNAMIC_STRING_CALLBACK</a>.
          The binary representation of the xml document references these strings by id (as opposed to embedding the actual string), 
          and therefore they must contain the same set of strings used when the document was written.
          The application that uses the reader and writer must coordinate communicating the values referenced by these strings.
        

