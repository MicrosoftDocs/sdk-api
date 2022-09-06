---
UID: NE:webservices.__unnamed_enum_0
title: WS_XML_READER_PROPERTY_ID (webservices.h)
description: Identifies each XML reader property is and its associated value.
helpviewer_keywords: ["WS_XML_READER_PROPERTY_ALLOW_FRAGMENT","WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES","WS_XML_READER_PROPERTY_CHARSET","WS_XML_READER_PROPERTY_COLUMN","WS_XML_READER_PROPERTY_ID","WS_XML_READER_PROPERTY_ID enumeration [Web Services for Windows]","WS_XML_READER_PROPERTY_IN_ATTRIBUTE","WS_XML_READER_PROPERTY_MAX_ATTRIBUTES","WS_XML_READER_PROPERTY_MAX_DEPTH","WS_XML_READER_PROPERTY_MAX_MIME_PARTS","WS_XML_READER_PROPERTY_MAX_NAMESPACES","WS_XML_READER_PROPERTY_READ_DECLARATION","WS_XML_READER_PROPERTY_ROW","WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE","WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE","WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE","WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE","webservices/WS_XML_READER_PROPERTY_ALLOW_FRAGMENT","webservices/WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES","webservices/WS_XML_READER_PROPERTY_CHARSET","webservices/WS_XML_READER_PROPERTY_COLUMN","webservices/WS_XML_READER_PROPERTY_ID","webservices/WS_XML_READER_PROPERTY_IN_ATTRIBUTE","webservices/WS_XML_READER_PROPERTY_MAX_ATTRIBUTES","webservices/WS_XML_READER_PROPERTY_MAX_DEPTH","webservices/WS_XML_READER_PROPERTY_MAX_MIME_PARTS","webservices/WS_XML_READER_PROPERTY_MAX_NAMESPACES","webservices/WS_XML_READER_PROPERTY_READ_DECLARATION","webservices/WS_XML_READER_PROPERTY_ROW","webservices/WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE","webservices/WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE","webservices/WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE","webservices/WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE","wsw.ws_xml_reader_property_id"]
old-location: wsw\ws_xml_reader_property_id.htm
tech.root: wsw
ms.assetid: b8d36716-e25a-4215-8bc7-30091b68c0f6
ms.date: 12/05/2018
ms.keywords: WS_XML_READER_PROPERTY_ALLOW_FRAGMENT, WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES, WS_XML_READER_PROPERTY_CHARSET, WS_XML_READER_PROPERTY_COLUMN, WS_XML_READER_PROPERTY_ID, WS_XML_READER_PROPERTY_ID enumeration [Web Services for Windows], WS_XML_READER_PROPERTY_IN_ATTRIBUTE, WS_XML_READER_PROPERTY_MAX_ATTRIBUTES, WS_XML_READER_PROPERTY_MAX_DEPTH, WS_XML_READER_PROPERTY_MAX_MIME_PARTS, WS_XML_READER_PROPERTY_MAX_NAMESPACES, WS_XML_READER_PROPERTY_READ_DECLARATION, WS_XML_READER_PROPERTY_ROW, WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE, WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE, WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE, WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE, webservices/WS_XML_READER_PROPERTY_ALLOW_FRAGMENT, webservices/WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES, webservices/WS_XML_READER_PROPERTY_CHARSET, webservices/WS_XML_READER_PROPERTY_COLUMN, webservices/WS_XML_READER_PROPERTY_ID, webservices/WS_XML_READER_PROPERTY_IN_ATTRIBUTE, webservices/WS_XML_READER_PROPERTY_MAX_ATTRIBUTES, webservices/WS_XML_READER_PROPERTY_MAX_DEPTH, webservices/WS_XML_READER_PROPERTY_MAX_MIME_PARTS, webservices/WS_XML_READER_PROPERTY_MAX_NAMESPACES, webservices/WS_XML_READER_PROPERTY_READ_DECLARATION, webservices/WS_XML_READER_PROPERTY_ROW, webservices/WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE, webservices/WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE, webservices/WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE, webservices/WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE, wsw.ws_xml_reader_property_id
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
targetos: Windows
req.typenames: WS_XML_READER_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_XML_READER_PROPERTY_ID
 - webservices/WS_XML_READER_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_READER_PROPERTY_ID
---

# WS_XML_READER_PROPERTY_ID enumeration


## -description

Identifies each XML reader property is and its associated
        value.  This enumeration is used within the <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_property">WS_XML_READER_PROPERTY</a> structure, which is used as a parameter to <a href="/windows/desktop/api/webservices/nf-webservices-wscreatereader">WsCreateReader</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a>, and <a href="/windows/desktop/api/webservices/nf-webservices-wsreadxmlbufferfrombytes">WsReadXmlBufferFromBytes</a>. It is also used directly as a parameter to <a href="/windows/desktop/api/webservices/nf-webservices-wsgetreaderproperty">WsGetReaderProperty</a>.

## -enum-fields

### -field WS_XML_READER_PROPERTY_MAX_DEPTH:0

A <b>ULONG</b> that specifies the maximum depth of the document that the reader will permit.
        

Depth is measured at any point by the number of nested start elements.
        

A depth of 0 prevents any start elements from being read.
        

This property defaults to 32.
        

See <a href="/windows/desktop/api/webservices/nf-webservices-wscreatereader">WsCreateReader</a> for security considerations.

### -field WS_XML_READER_PROPERTY_ALLOW_FRAGMENT:1

A <b>BOOL</b> that
          specifies whether the reader will permit multiple elements and non-white space at the top level of the document.  This property
          may not be set to <b>TRUE</b> with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_MTOM_ENCODING</a>.
        

This property defaults to <b>FALSE</b>.

### -field WS_XML_READER_PROPERTY_MAX_ATTRIBUTES:2

A <b>ULONG</b> that specifies the maximum number of attributes the reader will permit on an element.
        

This property defaults to 128.
        

See <a href="/windows/desktop/api/webservices/nf-webservices-wscreatereader">WsCreateReader</a> for security considerations.

### -field WS_XML_READER_PROPERTY_READ_DECLARATION:3

A <b>BOOL</b> that specifies if the reader should permit an xml declaration at the start of the document.
        

This property defaults to <b>TRUE</b>.

### -field WS_XML_READER_PROPERTY_CHARSET:4

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_charset">WS_CHARSET</a> value that returns the character set of the xml document.  This value is only available for
          text documents.
        

If the reader was initialized with a <a href="/windows/desktop/api/webservices/ne-webservices-ws_charset">WS_CHARSET_AUTO</a> then it will automatically determine this
          value.  The reader input source is streamed, then the reader must have enough data buffered to be able to
          inspect initial byte order marks and the xml declaration.  See <a href="/windows/desktop/api/webservices/nf-webservices-wsfillreader">WsFillReader</a>.
        

If the reader was initialized with any other value, then this property simply returns that value.

### -field WS_XML_READER_PROPERTY_ROW:5

A <b>ULONGLONG</b> that returns the 0 based row number of the node the reader is positioned on for text xml documents.

### -field WS_XML_READER_PROPERTY_COLUMN:6

A <b>ULONGLONG</b> that returns the 0 based column number of the node the reader is positioned on for text xml documents.

### -field WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE:7

A <b>ULONG</b> that specifies the trim size of the internal buffer used by the
          <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> for performing UTF-16 to UTF-8 conversions.  Increasing this value
          uses more memory, but can reduce allocations when processing UTF-16 encoded documents.
        

This property defaults to 4096.

### -field WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE:8

A <b>ULONG</b> that specifies the size of the buffer the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> will use when configured to use
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_stream_input">WS_XML_READER_STREAM_INPUT</a>.  Increasing this value uses more memory, but
          can reduce the number of times the <a href="/windows/desktop/api/webservices/nc-webservices-ws_read_callback">WS_READ_CALLBACK</a> is invoked.
        

This property defaults to 4096.

### -field WS_XML_READER_PROPERTY_IN_ATTRIBUTE:9

Indicates that <a href="/windows/desktop/api/webservices/nf-webservices-wsreadstartattribute">WsReadStartAttribute</a> has been called and the reader is
          positioned on attribute content.

### -field WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE:10

A <b>ULONG</b> used with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_STREAM_INPUT</a> in conjunction with <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_MTOM_ENCODING</a>.
          This value specifies the maximum size of the root MIME part, which is the part that contains
          the xml portion of the document.  It has no effect when used with other encodings, or when used with
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_buffer_input">WS_XML_READER_BUFFER_INPUT</a>.
        

This property defaults to 65536.

### -field WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE:11

A <b>ULONG</b> used with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_STREAM_INPUT</a> in conjunction with <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_MTOM_ENCODING</a>.
          This value specifies the maximum size of any group of MIME headers that may appear in the document.
          It has no effect when used with other encodings, or when used with <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_buffer_input">WS_XML_READER_BUFFER_INPUT</a>.
        

This property defaults to 256.

### -field WS_XML_READER_PROPERTY_MAX_MIME_PARTS:12

A <b>ULONG</b> used with  <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_MTOM_ENCODING</a>. This value specifies the maximum number of MIME parts
          that may appear in the document.  It has no effect when used with other encodings.
        

This property defaults to 4096.

### -field WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES:13

A <b>BOOL</b> used with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_text_encoding">WS_XML_READER_TEXT_ENCODING</a>. Setting this to <b>TRUE</b> permits character references
          of characters considered invalid by XML 1.0 to be accepted.
        

Setting this property to <b>TRUE</b> may affect interoperability.
        

This property defaults to <b>FALSE</b>.

### -field WS_XML_READER_PROPERTY_MAX_NAMESPACES:14

A <b>ULONG</b> that specifies the maximum number of xmlns unique declarations that may appear in scope at any point
          while reading the document.
        

This property defaults to 32.
        

See <a href="/windows/desktop/api/webservices/nf-webservices-wscreatereader">WsCreateReader</a> for security considerations.
