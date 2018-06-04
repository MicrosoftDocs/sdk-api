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

# _WS_XML_WRITER_RAW_ENCODING structure


## -description



        Used to indicate that the writer should emit bytes from decoded base64 characters.
      


## -struct-fields




### -field encoding


          The base type for all types that derive from <a href="https://msdn.microsoft.com/5ca43d39-e714-4070-b343-6c8ab9484817">WS_XML_WRITER_ENCODING</a>.
        


## -remarks




        This encoding can be useful when it is desirable to write an arbitrary, perhaps, non-xml document
        while still using the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> abstraction.  In this encoding, only characters
        representing base64 encoded bytes may be written, and only at the root of the document.  No
        elements or comments may be written.  The writer will emit the bytes represented by the base64 encoded 
        characters.  In order to accommodate non-whitespace text at the root of the document, the writer 
        will operate as if the <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT</a> property has been specified.
      


        The base64 characters of the document are only converted to bytes when necessary.  So, for example, 
        using <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a>, which normally performs a base64 encoding of the bytes it is passed,
        actually avoids all base64 conversions and is the most efficient way to write documents in this
        encoding. Using <a href="https://msdn.microsoft.com/e435058f-62b5-4ae9-800e-e022033a9664">WsWriteChars</a>, for example, will cause the base64 characters to physically get
        decoded to their corresponding bytes.  In general writing the document using anything other than 
        <a href="https://msdn.microsoft.com/02cff29c-7d39-4df2-8eb1-506f93959a1e">WsReadBytes</a>, <a href="https://msdn.microsoft.com/39e25db6-e51f-45cb-9739-260e7c246fcc">WsPullBytes</a>, or <a href="https://msdn.microsoft.com/295eb530-00f1-4e80-bd8a-ffb3eb1fad5b">WsPushBytes</a> will incur the 
        base64 conversion.
      



