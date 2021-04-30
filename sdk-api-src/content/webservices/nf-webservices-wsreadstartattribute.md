---
UID: NF:webservices.WsReadStartAttribute
title: WsReadStartAttribute function (webservices.h)
description: Moves the Reader to the specified attribute so that the content may be read using WsReadValue, WsReadChars, or WsReadBytes.
helpviewer_keywords: ["WsReadStartAttribute","WsReadStartAttribute function [Web Services for Windows]","webservices/WsReadStartAttribute","wsw.wsreadstartattribute"]
old-location: wsw\wsreadstartattribute.htm
tech.root: wsw
ms.assetid: 6fd0c8c2-2eac-4d98-898d-1c5849220c36
ms.date: 12/05/2018
ms.keywords: WsReadStartAttribute, WsReadStartAttribute function [Web Services for Windows], webservices/WsReadStartAttribute, wsw.wsreadstartattribute
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
 - WsReadStartAttribute
 - webservices/WsReadStartAttribute
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
 - WsReadStartAttribute
---

# WsReadStartAttribute function


## -description

Moves the Reader to the specified attribute so that the content may be read using <a href="/windows/desktop/api/webservices/nf-webservices-wsreadvalue">WsReadValue</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wsreadchars">WsReadChars</a>, or <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbytes">WsReadBytes</a>.
      
If the reader is not positioned on a start element then it returns a <b>WS_E_INVALID_FORMAT</b> exception.

(See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)<div class="alert"><b>Note</b>  Attributes read do not appear in any particular order.  <a href="/windows/desktop/api/webservices/nf-webservices-wsfindattribute">WsFindAttribute</a> can be used to locate the index of a particular attribute.
</div>
<div> </div>

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> object used to read the Start attribute.

### -param attributeIndex [in]

The index of the attribute to read.

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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a> function returns EOF when advanced within an attribute.  The <a href="/windows/desktop/api/webservices/nf-webservices-wsreadendattribute">WsReadEndAttribute</a> function can be used
        to return the reader to the containing element.