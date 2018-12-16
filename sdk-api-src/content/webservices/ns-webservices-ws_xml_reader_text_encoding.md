---
UID: NS:webservices._WS_XML_READER_TEXT_ENCODING
title: WS_XML_READER_TEXT_ENCODING
author: windows-sdk-content
description: Used to indicate that the reader should interpret the bytes it reads as textual xml.
old-location: wsw\ws_xml_reader_text_encoding.htm
tech.root: wsw
ms.assetid: ffb351d7-36dc-44ce-8a5e-ee452ca8b4e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_XML_READER_TEXT_ENCODING, WS_XML_READER_TEXT_ENCODING structure [Web Services for Windows], webservices/WS_XML_READER_TEXT_ENCODING, wsw.ws_xml_reader_text_encoding
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_READER_TEXT_ENCODING
product: Windows
targetos: Windows
req.typenames: WS_XML_READER_TEXT_ENCODING
req.redist: 
---

# WS_XML_READER_TEXT_ENCODING structure


## -description


Used to indicate that the reader should interpret the bytes it reads as textual xml.
      


## -struct-fields




### -field encoding

The base type for all types that derive from <a href="https://msdn.microsoft.com/54d9683e-c2d1-4e18-92a2-a68558999e28">WS_XML_READER_ENCODING</a>.
        


### -field charSet

Indicates the text encoding of the bytes.  If <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_AUTO</a> is specified then the reader will
          determine the encoding of the document based on the first few bytes of the document.  If an xml declaration
          is present in the document, the reader will ensure that the encoding attribute coincides with this value.
        

