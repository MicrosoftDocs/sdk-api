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

# _WS_XML_READER_RAW_ENCODING structure


## -description



        Used to indicate that the reader should surface the bytes of the document as base64 encoded characters.
      


## -struct-fields




### -field encoding


          The base type for all types that derive from <a href="https://msdn.microsoft.com/54d9683e-c2d1-4e18-92a2-a68558999e28">WS_XML_READER_ENCODING</a>.
        


## -remarks




        This encoding can be useful when it is desirable to read an arbitrary, perhaps, non-xml document
        while still using the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> abstraction.  In this encoding, the bytes comprising
        the document are presented as base64 encoded characters at the root of a xml document.  In order to
        accommodate non-whitespace text at the root of the document, the reader will operate as if the
        <a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_ALLOW_FRAGMENT</a> property has been specified.
      


        The bytes of the document are only converted to base64 when necessary.  So, for example, using 
        <a href="https://msdn.microsoft.com/02cff29c-7d39-4df2-8eb1-506f93959a1e">WsReadBytes</a>, which normally performs a base64 decoding of the characters it reads, 
        actually avoids all base64 conversions and is the most efficient way to read documents in this
        encoding. Using <a href="https://msdn.microsoft.com/3285d3f7-8ab1-42f0-b6e0-1d91aa0d576f">WsReadChars</a>, for example, will cause the bytes to physically get 
        converted to their corresponding base64 characters.  In general reading the document using
        anything other than <b>WsReadBytes</b> will incur the base64 conversion.
      



