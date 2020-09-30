---
UID: NF:webservices.WsGetWriterProperty
title: WsGetWriterProperty function (webservices.h)
description: Retrieves a specified XML Writer property. The property to retrieve is identified by a WS_XML WRITER_PROPERTY_ID input parameter.
helpviewer_keywords: ["WsGetWriterProperty","WsGetWriterProperty function [Web Services for Windows]","webservices/WsGetWriterProperty","wsw.wsgetwriterproperty"]
old-location: wsw\wsgetwriterproperty.htm
tech.root: wsw
ms.assetid: 1167662f-0383-44bb-a7e1-1ec12539903e
ms.date: 12/05/2018
ms.keywords: WsGetWriterProperty, WsGetWriterProperty function [Web Services for Windows], webservices/WsGetWriterProperty, wsw.wsgetwriterproperty
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
 - WsGetWriterProperty
 - webservices/WsGetWriterProperty
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
 - WsGetWriterProperty
---

# WsGetWriterProperty function


## -description

Retrieves a specified XML Writer property.  The property to retrieve is identified by a  <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_writer_property_id">WS_XML WRITER_PROPERTY_ID</a> input parameter.

## -parameters

### -param writer [in]

A pointer  to a WS_XML_WRITER structure that contains the property value to retrieve.

### -param id [in]

This is a <b>WS_XML_WRITER_PROPERTY_ID</b> enumerator that identifies the property to retrieve.

### -param value

A void pointer to a location for storing the retrieved property value.

### -param valueSize [in]

The byte-length buffer size allocated by the caller to store the retrieved property value.
                The pointer must have an alignment compatible with the type
            of the property.

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