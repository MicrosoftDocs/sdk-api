---
UID: NF:webservices.WsWriteEndStartElement
title: WsWriteEndStartElement function (webservices.h)
description: Forces the writer to commit the current element and prevent further attributes from being written to the element.
helpviewer_keywords: ["WsWriteEndStartElement","WsWriteEndStartElement function [Web Services for Windows]","webservices/WsWriteEndStartElement","wsw.wswriteendstartelement"]
old-location: wsw\wswriteendstartelement.htm
tech.root: wsw
ms.assetid: 56bf55f8-978c-4f03-9ace-f992530927c2
ms.date: 12/05/2018
ms.keywords: WsWriteEndStartElement, WsWriteEndStartElement function [Web Services for Windows], webservices/WsWriteEndStartElement, wsw.wswriteendstartelement
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
 - WsWriteEndStartElement
 - webservices/WsWriteEndStartElement
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
 - WsWriteEndStartElement
---

# WsWriteEndStartElement function


## -description

Forces the writer to commit the current element and prevent further attributes 
        from being written to the element.

## -parameters

### -param writer [in]

The writer for which the current element should be committed.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

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
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>

## -remarks

Occasionally, it is useful to explicitly force the completion of an element.  This can be used to force the writer
        to write a full element and pair.  It also may be useful when obtaining positions when writing to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.
      

Calling this API when there is no element to commit will cause it to return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)