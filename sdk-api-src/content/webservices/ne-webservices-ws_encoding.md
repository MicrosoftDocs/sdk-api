---
UID: NE:webservices.WS_ENCODING
title: WS_ENCODING
author: windows-sdk-content
description: The different encodings (message formats).
old-location: wsw\ws_encoding.htm
tech.root: wsw
ms.assetid: 37858df7-ae76-41c1-8fd2-fc810b8927bf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_ENCODING, WS_ENCODING enumeration [Web Services for Windows], WS_ENCODING_XML_BINARY_1, WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_MTOM_UTF16BE, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_UTF16BE, WS_ENCODING_XML_UTF16LE, WS_ENCODING_XML_UTF8, webservices/WS_ENCODING, webservices/WS_ENCODING_XML_BINARY_1, webservices/WS_ENCODING_XML_BINARY_SESSION_1, webservices/WS_ENCODING_XML_MTOM_UTF16BE, webservices/WS_ENCODING_XML_MTOM_UTF16LE, webservices/WS_ENCODING_XML_MTOM_UTF8, webservices/WS_ENCODING_XML_UTF16BE, webservices/WS_ENCODING_XML_UTF16LE, webservices/WS_ENCODING_XML_UTF8, wsw.ws_encoding
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
 - WS_ENCODING
product: Windows
targetos: Windows
req.typenames: WS_ENCODING
req.redist: 
---

# WS_ENCODING enumeration


## -description


The different encodings (message formats).
            


## -enum-fields




### -field WS_ENCODING_XML_BINARY_1

The binary XML encoding.
                

Although the data is still in the XML
                    infoset format, this encoding typically results in smaller messages
                    that require less CPU to produce and consume.
                

This encoding requires SOAP 1.2 (<a href="https://msdn.microsoft.com/2a6f6148-d37d-4ac2-8fd0-409eae71a3d8">WS_ENVELOPE_VERSION_SOAP_1_2</a>).
                


### -field WS_ENCODING_XML_BINARY_SESSION_1

The binary XML session encoding.
                

Although the data is still in the XML
                    infoset format, this encoding typically results in smaller messages
                    that require less CPU to produce and consume.
                

This encoding is like <a href="https://msdn.microsoft.com/37858df7-ae76-41c1-8fd2-fc810b8927bf">WS_ENCODING_XML_BINARY_1</a> but adds the
                    feature of a session dictionary.  Because this encoding requires a
                    session, it may only be used on sessionful channel types
                    (<a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_DUPLEX_SESSION</a>).
                

The session dictionary is a data structure maintained by both the
                    sending and receiving side of a channel.  The session dictionary
                    is used to optimize the transmission of string data.  The first time
                    a particular string is written, it is encoded using in the full string
                    format.  If the same string is written again, then it will use a smaller
                    tokenized form, which can reduce message size.
                

The writer of the string data selects which strings are candidates for
                    the session dictionary by filling out the dictionary and id fields of 
                    the <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> structure.
                

The size of the session dictionary is configured using 
                    <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_MAX_SESSION_DICTIONARY_SIZE</a>.
                

This encoding requires SOAP 1.2 (<a href="https://msdn.microsoft.com/2a6f6148-d37d-4ac2-8fd0-409eae71a3d8">WS_ENVELOPE_VERSION_SOAP_1_2</a>).
                


### -field WS_ENCODING_XML_MTOM_UTF8

The MTOM encoding.
                

The MTOM encoding optimizes for binary data by avoiding the costs
                    of converting binary data to base64 format.  For messages containing
                    large amounts of binary data, this encoding usually results in smaller
                    messages that require less CPU to produce and consume
                    than with a text encoding.  This encoding is typically not as efficient as
                    a binary encoding, however.
                

The XML part of the MTOM package is written
                    using <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_UTF8</a>, but may be in any <b>WS_CHARSET</b>when read.
                


### -field WS_ENCODING_XML_MTOM_UTF16BE

The MTOM encoding.
                

The MTOM encoding optimizes for binary data by avoiding the costs
                    of converting binary data to base64 format.  For messages containing
                    large amounts of binary data, this encoding usually results in smaller
                    messages that require less CPU to produce and consume
                    than with a text encoding.  This encoding is typically not as efficient as
                    a binary encoding, however.
                

The XML part of the MTOM package is written
                    using <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_UTF16BE</a>, but may be in any <b>WS_CHARSET</b>when read.
                


### -field WS_ENCODING_XML_MTOM_UTF16LE

The MTOM encoding.
                

The MTOM encoding optimizes for binary data by avoiding the costs
                    of converting binary data to base64 format.  For messages containing
                    large amounts of binary data, this encoding usually results in smaller
                    messages that require less CPU to produce and consume
                    than with a text encoding.  This encoding is typically not as efficient as
                    a binary encoding, however.
                

The XML part of the MTOM package is written
                    using <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_UTF16LE</a>, but may be in any <b>WS_CHARSET</b>when read.
                


### -field WS_ENCODING_XML_UTF8

The text encoding (XML 1.0 format).
                

Data is written using <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_UTF8</a>,
                    but may be in any <b>WS_CHARSET</b> when read.
                


### -field WS_ENCODING_XML_UTF16BE

The text encoding (XML 1.0 format).
                

Data is written using <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_UTF16BE</a>,
                    but may be in any <b>WS_CHARSET</b> when read.
                


### -field WS_ENCODING_XML_UTF16LE

The text encoding (XML 1.0 format).
                

Data is written using <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET_UTF16LE</a>,
                    but may be in any <b>WS_CHARSET</b> when read.
                


### -field WS_ENCODING_RAW



