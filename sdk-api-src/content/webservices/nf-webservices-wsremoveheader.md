---
UID: NF:webservices.WsRemoveHeader
title: WsRemoveHeader function (webservices.h)
description: Removes the standard WS_HEADER_TYPE object from a message.
helpviewer_keywords: ["WsRemoveHeader","WsRemoveHeader function [Web Services for Windows]","webservices/WsRemoveHeader","wsw.wsremoveheader"]
old-location: wsw\wsremoveheader.htm
tech.root: wsw
ms.assetid: b240acbd-2c0e-4e2c-a334-a86440627e72
ms.date: 12/05/2018
ms.keywords: WsRemoveHeader, WsRemoveHeader function [Web Services for Windows], webservices/WsRemoveHeader, wsw.wsremoveheader
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
 - WsRemoveHeader
 - webservices/WsRemoveHeader
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
 - WsRemoveHeader
---

# WsRemoveHeader function


## -description

Removes the standard <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a> object from a message.
                
The function is designed to handle types of headers that appear once in the message and are targeted at the ultimate receiver. Headers targeted with a role other than ultimate receiver are ignored.

For application-defined header types use the <a href="/windows/desktop/api/webservices/nf-webservices-wsremovecustomheader">WsRemoveCustomHeader</a> function.

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object with the header  to be removed. The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b>.

### -param headerType [in]

Indicates the type of header to be removed.

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
There are multiple instances of the type of header present in the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

If a header of the given type exists in the message it is removed.  If the header does not exist, no action is taken
                and the function completes successfully.