---
UID: NF:webservices.WsSetInput
title: WsSetInput function (webservices.h)
description: Sets the encoding and input sources for an XML Reader.
helpviewer_keywords: ["WsSetInput","WsSetInput function [Web Services for Windows]","webservices/WsSetInput","wsw.wssetinput"]
old-location: wsw\wssetinput.htm
tech.root: wsw
ms.assetid: d7ac5233-266e-4ca1-aa58-e50b385b48bb
ms.date: 12/05/2018
ms.keywords: WsSetInput, WsSetInput function [Web Services for Windows], webservices/WsSetInput, wsw.wssetinput
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
 - WsSetInput
 - webservices/WsSetInput
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
 - WsSetInput
---

# WsSetInput function


## -description

Sets the encoding and input sources for an XML  Reader.
      These settings override settings made when the Reader was created.<div class="alert"><b>Note</b>  If both encoding and input are <b>NULL</b> the reader will operate as if it is positioned at the end of an empty XML document.
      </div>
<div> </div>

## -parameters

### -param reader [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object for which the input will be set.

### -param encoding [in, optional]

A to an encoding value that describes the format of the input bytes.  This value should be one of:<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_text_encoding">WS_XML_READER_TEXT_ENCODING</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_binary_encoding">WS_XML_READER_BINARY_ENCODING</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_xml_reader_mtom_encoding">WS_XML_READER_MTOM_ENCODING</a>
</li>
</ul>

### -param input [in, optional]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_input">WS_XML_READER_INPUT</a> structure that indicates the reader type.

### -param properties

An array reference of optional Reader properties.

### -param propertyCount [in]

The number of properties.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When <b>WsSetInput</b> is used on the XML Reader, the reader will function in a forward only manner and
        the functions <a href="/windows/desktop/api/webservices/nf-webservices-wsgetreaderposition">WsGetReaderPosition</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wssetreaderposition">WsSetReaderPosition</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsmovereader">WsMoveReader</a> cannot be used.