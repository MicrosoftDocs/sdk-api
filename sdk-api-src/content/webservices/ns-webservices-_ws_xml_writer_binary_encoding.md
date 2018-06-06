---
UID: NS:webservices._WS_XML_WRITER_BINARY_ENCODING
title: "_WS_XML_WRITER_BINARY_ENCODING"
author: windows-sdk-content
description: Used to indicate that the writer should emit bytes as binary xml.
old-location: wsw\ws_xml_writer_binary_encoding.htm
old-project: wsw
ms.assetid: b4485490-b5e1-406c-883c-a30bfa334316
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_XML_WRITER_BINARY_ENCODING, WS_XML_WRITER_BINARY_ENCODING structure [Web Services for Windows], _WS_XML_WRITER_BINARY_ENCODING, webservices/WS_XML_WRITER_BINARY_ENCODING, wsw.ws_xml_writer_binary_encoding
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_XML_WRITER_BINARY_ENCODING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_WRITER_BINARY_ENCODING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_WRITER_BINARY_ENCODING structure


## -description



        Used to indicate that the writer should emit bytes as binary xml.
      


## -struct-fields




### -field encoding


          The base type for all types that derive from <a href="https://msdn.microsoft.com/5ca43d39-e714-4070-b343-6c8ab9484817">WS_XML_WRITER_ENCODING</a>.
        


### -field staticDictionary


          Indicates the dictionary that the writer should use for static strings.  <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a>s that are written that
          reference this dictionary, will be written in the binary xml document using an id rather than the string itself.
          When reading this document, the application must provide a dictionary with the same strings.
        


### -field dynamicStringCallback


          Specifies an optional callback that the writer will invoke when a <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> that is not found in the staticDictionary is written for the first time.
          The callback provides the mapping to an id which the writer will then use.  It is the responsibility of the callback to coordinate with the
          writer to propagate these strings to the reader. The string is not added to the dictionary if this callback is not specified.
        


### -field dynamicStringCallbackState


          User-defined state that will be passed to dynamicStringCallback.
        

