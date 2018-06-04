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

# _WS_XML_READER_MTOM_ENCODING structure


## -description



        Used to indicate that the reader should interpret the bytes it reads as in MTOM format.
      


## -struct-fields




### -field encoding


          The base type for all types that derive from <a href="https://msdn.microsoft.com/54d9683e-c2d1-4e18-92a2-a68558999e28">WS_XML_READER_ENCODING</a>.
        


### -field textEncoding

The encoding of the xml document carried by MTOM.
        


### -field readMimeHeader


          Specifies whether or not the reader should read the MIME header.
        


### -field startInfo


          The type used by the mime part that contains the xml.  This corresponds to the "start-info" parameter in the of the MIME Content-Type.
          If readMimeHeader is specified as <b>TRUE</b>, then this must be empty as the startInfo will be read from the mime header.
        


### -field boundary


          The character sequence that should be used to delimit the mime parts.  This corresponds to the "boundary" parameter of the MIME Content-Type.
          If readMimeHeader is specified as <b>TRUE</b>, then this must be empty as the boundary will be read from the mime header.
        


### -field startUri


          The mime part that contains the xml.  This corresponds to the "start" parameter of the MIME Content-Type.
          If readMimeHeader is specified as <b>TRUE</b>, then this must be empty as the startUri will be read from the mime header.
        


## -remarks




        When used with <a href="https://msdn.microsoft.com/86277c29-d42f-4b6a-ba33-b836bef284e7">WS_XML_READER_BUFFER_INPUT</a> the MIME parts may appear in any order.
      


        When used with <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a> the root MIME part must be first, and
        subsequent MIME parts must appear in the order that they are referenced from xop:Include elements.
      


        See http://www.w3.org/TR/2005/REC-xop10-20050125/ for the MTOM specification.
      



