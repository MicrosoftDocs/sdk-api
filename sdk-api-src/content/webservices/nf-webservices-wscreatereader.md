---
UID: NF:webservices.WsCreateReader
title: WsCreateReader function (webservices.h)
description: Creates an XML reader with the specified properties.
helpviewer_keywords: ["WsCreateReader","WsCreateReader function [Web Services for Windows]","webservices/WsCreateReader","wsw.wscreatereader"]
old-location: wsw\wscreatereader.htm
tech.root: wsw
ms.assetid: 0d4449aa-ffcc-41d9-99b1-7352edaf3700
ms.date: 12/05/2018
ms.keywords: WsCreateReader, WsCreateReader function [Web Services for Windows], webservices/WsCreateReader, wsw.wscreatereader
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsCreateReader
 - webservices/WsCreateReader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCreateReader
---

# WsCreateReader function


## -description

Creates an <a href="/windows/desktop/wsw/xml-reader">XML reader</a> with the specified properties.

## -parameters

### -param properties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_property">WS_XML_READER_PROPERTY</a> structures containing optional properties for the XML reader.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                

For the properties that tiy can use to configure the XML reader, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_reader_property_id">WS_XML_READER_PROPERTY_ID</a> enumeration.

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param reader

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> structure representing the new XML reader.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreereader">WsFreeReader</a>.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

## -remarks

Use <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a> functions to choose the encoding for the XML reader and to indicate the source of the input.
      

If <a href="/windows/desktop/api/webservices/nc-webservices-ws_read_callback">WS_READ_CALLBACK</a> is specified in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_input">WS_XML_READER_INPUT</a> structure passed to the <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> function, the XML reader reads
        additional data only when <a href="/windows/desktop/api/webservices/nf-webservices-wsfillreader">WsFillReader</a> is called.  This allows the caller to determine
        at what granularity to read data and whether to read that data asynchronously.
      

A <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> structure can be reused by calling <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a> again.
      

If any API operation that operates on an <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> fails the XML reader is left in a faulted state
        and further function calls return <b>WS_E_OBJECT_FAULTED</b>.  (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.) The only possible function calls for the XML reader
        if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a> for returning the XML reader to a usable state,
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreereader">WsFreeReader</a> for releasing the XML reader object.