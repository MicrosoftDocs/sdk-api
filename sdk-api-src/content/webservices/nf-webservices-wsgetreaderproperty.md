---
UID: NF:webservices.WsGetReaderProperty
title: WsGetReaderProperty function (webservices.h)
description: This function returns a property of the specified XML Reader.
helpviewer_keywords: ["WsGetReaderProperty","WsGetReaderProperty function [Web Services for Windows]","webservices/WsGetReaderProperty","wsw.wsgetreaderproperty"]
old-location: wsw\wsgetreaderproperty.htm
tech.root: wsw
ms.assetid: 32a42d65-c551-4a40-b44d-5ef44e782d30
ms.date: 12/05/2018
ms.keywords: WsGetReaderProperty, WsGetReaderProperty function [Web Services for Windows], webservices/WsGetReaderProperty, wsw.wsgetreaderproperty
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
 - WsGetReaderProperty
 - webservices/WsGetReaderProperty
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
 - WsGetReaderProperty
---

# WsGetReaderProperty function


## -description

This function returns a property of the specified XML Reader.
<div class="alert"><b>Note</b>  Obtaining the Property <b>WS_XML_READER_PROPERTY_CHARSET</b> will require inspecting up to the first
        four bytes of the XML data.  Consequently if the Reader is using <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_stream_input">WS_XML_READER_STREAM_INPUT</a> the
        <a href="/windows/desktop/api/webservices/nf-webservices-wsfillreader">WsFillReader</a> function must be called first to ensure that this data has been read.</div><div> </div>

## -parameters

### -param reader [in]

A pointer to a WS_XML_READER object containing the desired property value.

### -param id [in]

An enumerator value identifier of the Reader property.

### -param value

A pointer to the address for returning the retrieved value.
            The pointer must have an alignment compatible with the type
            of the property.

### -param valueSize [in]

A byte count of the buffer that the caller has allocated for the retrieved value.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property id was not supported for this object or the specified buffer was not large enough for the value.

</td>
</tr>
</table>