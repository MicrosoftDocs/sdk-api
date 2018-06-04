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

# _WS_XML_WRITER_MTOM_ENCODING structure


## -description



        Used to indicate that the reader should emit bytes in MTOM format.  
        The MTOM format will represent bytes written to it as binary mime 
        parts rather than embedded base64 encoded text.
      


## -struct-fields




### -field encoding


          The base type for all types that derive from <a href="https://msdn.microsoft.com/5ca43d39-e714-4070-b343-6c8ab9484817">WS_XML_WRITER_ENCODING</a>.
        


### -field textEncoding


          Specifies the encoding of the xml document carried by MTOM.
        


### -field writeMimeHeader


          Specifies whether or not the writer should emit a MIME header.
        


### -field boundary


          Specifies the character sequence that should be used to delimit the mime parts.  This corresponds to the "boundary" parameter of the MIME Content-Type.
        


### -field startInfo


          Specifies the type used by the mime part that contains the xml.  This correpsonds to the "start-info" parameter in the of the MIME Content-Type.
        


### -field startUri


          Specifies the mime part that contains the xml.  This corresponds to the "start" parameter of the MIME Content-Type.
        


### -field maxInlineByteCount


          Specifies the threshold at which the writer will not write base64 encoded text and instead write a binary mime part for binary data.
        

