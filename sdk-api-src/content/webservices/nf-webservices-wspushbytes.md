---
UID: NF:webservices.WsPushBytes
title: WsPushBytes function (webservices.h)
description: Establishes a callback to be invoked to write bytes within an element. In some encodings this can be more efficient by eliminating a copy of the data.
helpviewer_keywords: ["WsPushBytes","WsPushBytes function [Web Services for Windows]","webservices/WsPushBytes","wsw.wspushbytes"]
old-location: wsw\wspushbytes.htm
tech.root: wsw
ms.assetid: 295eb530-00f1-4e80-bd8a-ffb3eb1fad5b
ms.date: 12/05/2018
ms.keywords: WsPushBytes, WsPushBytes function [Web Services for Windows], webservices/WsPushBytes, wsw.wspushbytes
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
 - WsPushBytes
 - webservices/WsPushBytes
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
 - WsPushBytes
---

# WsPushBytes function


## -description

Establishes a callback to be invoked to write bytes within an element.  In some encodings this can
        be more efficient by eliminating a copy of the data.

## -parameters

### -param writer [in]

A pointer to the XML Writer object to which the bytes are written.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> and   the referenced value may not be <b>NULL</b>.

### -param callback [in]

This parameter is the callback to invoke to write the data.

### -param callbackState [in, optional]

A pointer to a user-defined state that is  passed to the callback function.

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
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>

## -remarks

When writing with the <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_mtom_encoding">WS_XML_WRITER_MTOM_ENCODING</a>, <b>WsPushBytes</b> provides a way
        to write bytes directly into its own MIME part and avoid a copy.  However, the writer at its discretion,
        may choose to invoke the callback immediately, so the caller should be prepared for this.
      

If the encoding cannot take advantage of this behavior, then <b>WsPushBytes</b> will invoke the
        callback immediately and operate as if <a href="/windows/desktop/api/webservices/nf-webservices-wswritebytes">WsWriteBytes</a> was called.