---
UID: NE:webservices.WS_XML_READER_PROPERTY_ID
title: WS_XML_READER_PROPERTY_ID
author: windows-sdk-content
description: Identifies each XML reader property is and its associated value.
old-location: wsw\ws_xml_reader_property_id.htm
tech.root: wsw
ms.assetid: b8d36716-e25a-4215-8bc7-30091b68c0f6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_XML_READER_PROPERTY_ALLOW_FRAGMENT, WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES, WS_XML_READER_PROPERTY_CHARSET, WS_XML_READER_PROPERTY_COLUMN, WS_XML_READER_PROPERTY_ID, WS_XML_READER_PROPERTY_ID enumeration [Web Services for Windows], WS_XML_READER_PROPERTY_IN_ATTRIBUTE, WS_XML_READER_PROPERTY_MAX_ATTRIBUTES, WS_XML_READER_PROPERTY_MAX_DEPTH, WS_XML_READER_PROPERTY_MAX_MIME_PARTS, WS_XML_READER_PROPERTY_MAX_NAMESPACES, WS_XML_READER_PROPERTY_READ_DECLARATION, WS_XML_READER_PROPERTY_ROW, WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE, WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE, WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE, WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE, webservices/WS_XML_READER_PROPERTY_ALLOW_FRAGMENT, webservices/WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES, webservices/WS_XML_READER_PROPERTY_CHARSET, webservices/WS_XML_READER_PROPERTY_COLUMN, webservices/WS_XML_READER_PROPERTY_ID, webservices/WS_XML_READER_PROPERTY_IN_ATTRIBUTE, webservices/WS_XML_READER_PROPERTY_MAX_ATTRIBUTES, webservices/WS_XML_READER_PROPERTY_MAX_DEPTH, webservices/WS_XML_READER_PROPERTY_MAX_MIME_PARTS, webservices/WS_XML_READER_PROPERTY_MAX_NAMESPACES, webservices/WS_XML_READER_PROPERTY_READ_DECLARATION, webservices/WS_XML_READER_PROPERTY_ROW, webservices/WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE, webservices/WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE, webservices/WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE, webservices/WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE, wsw.ws_xml_reader_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WS_XML_READER_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: WS_XML_READER_PROPERTY_ID
req.redist: 
---

# WS_XML_READER_PROPERTY_ID enumeration


## -description


Identifies each XML reader property is and its associated
        value.  This enumeration is used within the <a href="https://msdn.microsoft.com/8864d679-c321-45bb-b774-f05696d6098e">WS_XML_READER_PROPERTY</a> structure, which is used as a parameter to <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a>, <a href="https://msdn.microsoft.com/d7ac5233-266e-4ca1-aa58-e50b385b48bb">WsSetInput</a>, <a href="https://msdn.microsoft.com/0b3ac6ab-8c16-4189-950d-84bdcdabcde0">WsSetInputToBuffer</a>, and <a href="https://msdn.microsoft.com/7ab68738-add0-4e2a-a036-5c6ecdd1f236">WsReadXmlBufferFromBytes</a>. It is also used directly as a parameter to <a href="https://msdn.microsoft.com/32a42d65-c551-4a40-b44d-5ef44e782d30">WsGetReaderProperty</a>.
      


## -enum-fields




### -field WS_XML_READER_PROPERTY_MAX_DEPTH

A <b>ULONG</b> that specifies the maximum depth of the document that the reader will permit.
        

Depth is measured at any point by the number of nested start elements.
        

A depth of 0 prevents any start elements from being read.
        

This property defaults to 32.
        

See <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a> for security considerations.
        


### -field WS_XML_READER_PROPERTY_ALLOW_FRAGMENT

A <b>BOOL</b> that
          specifies whether the reader will permit multiple elements and non-white space at the top level of the document.  This property
          may not be set to <b>TRUE</b> with <a href="https://msdn.microsoft.com/dec4d9ad-71d3-48f9-b6c3-49cf6bcb85fb">WS_XML_READER_MTOM_ENCODING</a>.
        

This property defaults to <b>FALSE</b>.
        


### -field WS_XML_READER_PROPERTY_MAX_ATTRIBUTES

A <b>ULONG</b>that specifies the maximum number of attributes the reader will permit on an element.
        

This property defaults to 128.
        

See <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a> for security considerations.
        


### -field WS_XML_READER_PROPERTY_READ_DECLARATION

A <b>BOOL</b> that specifies if the reader should permit an xml declaration at the start of the document.
        

This property defaults to <b>TRUE</b>.
        


### -field WS_XML_READER_PROPERTY_CHARSET

A <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET</a> value that returns the character set of the xml document.  This value is only available for
          text documents.
        

If the reader was initialized with a <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_AUTO</a> then it will automatically determine this
          value.  The reader input source is streamed, then the reader must have enough data buffered to be able to
          inspect initial byte order marks and the xml declaration.  See <a href="https://msdn.microsoft.com/1f4138a2-acc5-4f1d-8e35-544859d2fa49">WsFillReader</a>.
        

If the reader was initialized with any other value, then this property simply returns that value.
        


### -field WS_XML_READER_PROPERTY_ROW

A <b>ULONGLONG</b> that returns the 0 based row number of the node the reader is positioned on for text xml documents.
        


### -field WS_XML_READER_PROPERTY_COLUMN

A <b>ULONGLONG</b> that returns the 0 based column number of the node the reader is positioned on for text xml documents.
        


### -field WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE

A <b>ULONG</b> that specifies the trim size of the internal buffer used by the
          <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> for performing UTF-16 to UTF-8 conversions.  Increasing this value
          uses more memory, but can reduce allocations when processing UTF-16 encoded documents.
        

This property defaults to 4096.
        


### -field WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE

A <b>ULONG</b> that specifies the size of the buffer the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> will use when configured to use
          <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a>.  Increasing this value uses more memory, but
          can reduce the number of times the <a href="https://msdn.microsoft.com/2a5ebe4a-e97d-4744-9ec9-da6da892e4c5">WS_READ_CALLBACK</a> is invoked.
        

This property defaults to 4096.          
        


### -field WS_XML_READER_PROPERTY_IN_ATTRIBUTE

Indicates that <a href="https://msdn.microsoft.com/6fd0c8c2-2eac-4d98-898d-1c5849220c36">WsReadStartAttribute</a> has been called and the reader is
          positioned on attribute content.
        
      


### -field WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE

A <b>ULONG</b>used with <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a> in conjunction with <a href="https://msdn.microsoft.com/dec4d9ad-71d3-48f9-b6c3-49cf6bcb85fb">WS_XML_READER_MTOM_ENCODING</a>.
          This value specifies the maximum size of the root MIME part, which is the part that contains
          the xml portion of the document.  It has no effect when used with other encodings, or when used with
          <a href="https://msdn.microsoft.com/86277c29-d42f-4b6a-ba33-b836bef284e7">WS_XML_READER_BUFFER_INPUT</a>.
        

This property defaults to 65536.          
        


### -field WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE

A <b>ULONG</b>used with <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a> in conjunction with <a href="https://msdn.microsoft.com/dec4d9ad-71d3-48f9-b6c3-49cf6bcb85fb">WS_XML_READER_MTOM_ENCODING</a>.
          This value specifies the maximum size of any group of MIME headers that may appear in the document.
          It has no effect when used with other encodings, or when used with <a href="https://msdn.microsoft.com/86277c29-d42f-4b6a-ba33-b836bef284e7">WS_XML_READER_BUFFER_INPUT</a>.
        

This property defaults to 256.
        


### -field WS_XML_READER_PROPERTY_MAX_MIME_PARTS

A <b>ULONG</b>used with  <a href="https://msdn.microsoft.com/dec4d9ad-71d3-48f9-b6c3-49cf6bcb85fb">WS_XML_READER_MTOM_ENCODING</a>. This value specifies the maximum number of MIME parts
          that may appear in the document.  It has no effect when used with other encodings.
        

This property defaults to 4096.          
        


### -field WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES

A <b>BOOL</b> used with <a href="https://msdn.microsoft.com/ffb351d7-36dc-44ce-8a5e-ee452ca8b4e6">WS_XML_READER_TEXT_ENCODING</a>. Setting this to <b>TRUE</b> permits character references
          of characters considered invalid by XML 1.0 to be accepted.
        

Setting this property to <b>TRUE</b> may affect interoperability.
        

This property defaults to <b>FALSE</b>.
        


### -field WS_XML_READER_PROPERTY_MAX_NAMESPACES

A <b>ULONG</b>that specifies the maximum number of xmlns unique declarations that may appear in scope at any point
          while reading the document.
        

This property defaults to 32.
        

See <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a> for security considerations.
        

