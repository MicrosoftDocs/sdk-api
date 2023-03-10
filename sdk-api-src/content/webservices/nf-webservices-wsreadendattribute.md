---
UID: NF:webservices.WsReadEndAttribute
title: WsReadEndAttribute function (webservices.h)
description: Moves the reader back to the element node containing the attribute that was read.
helpviewer_keywords: ["WsReadEndAttribute","WsReadEndAttribute function [Web Services for Windows]","webservices/WsReadEndAttribute","wsw.wsreadendattribute"]
old-location: wsw\wsreadendattribute.htm
tech.root: wsw
ms.assetid: 1181ca68-f67b-47e1-b9de-1bc57ecf36f6
ms.date: 12/05/2018
ms.keywords: WsReadEndAttribute, WsReadEndAttribute function [Web Services for Windows], webservices/WsReadEndAttribute, wsw.wsreadendattribute
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
 - WsReadEndAttribute
 - webservices/WsReadEndAttribute
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
 - WsReadEndAttribute
---

# WsReadEndAttribute function


## -description

Moves the reader back to the element node containing the attribute that was read.

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> that reads the <b>End attribute</b>.
                  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object.

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

<a href="/windows/desktop/api/webservices/nf-webservices-wsreadstartattribute">WsReadStartAttribute</a> must have been called in order to use this API.