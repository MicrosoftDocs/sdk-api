---
UID: NS:webservices._WS_XML_READER_RAW_ENCODING
title: "_WS_XML_READER_RAW_ENCODING"
author: windows-sdk-content
description: Used to indicate that the reader should surface the bytes of the document as base64 encoded characters.
old-location: wsw\ws_xml_reader_raw_encoding.htm
old-project: wsw
ms.assetid: 5f3004e7-347f-46a5-8d8f-743a76e1fa71
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_XML_READER_RAW_ENCODING, WS_XML_READER_RAW_ENCODING structure [Web Services for Windows], _WS_XML_READER_RAW_ENCODING, webservices/WS_XML_READER_RAW_ENCODING, wsw.ws_xml_reader_raw_encoding
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
req.typenames: WS_XML_READER_RAW_ENCODING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_READER_RAW_ENCODING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
      



