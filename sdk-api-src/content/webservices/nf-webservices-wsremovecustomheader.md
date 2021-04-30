---
UID: NF:webservices.WsRemoveCustomHeader
title: WsRemoveCustomHeader function (webservices.h)
description: Removes a custom header from the message. This function is designed to handle types of headers that appear once in the message and are targeted at the ultimate receiver. Headers targeted with a role other than ultimate receiver are ignored.
helpviewer_keywords: ["WsRemoveCustomHeader","WsRemoveCustomHeader function [Web Services for Windows]","webservices/WsRemoveCustomHeader","wsw.wsremovecustomheader"]
old-location: wsw\wsremovecustomheader.htm
tech.root: wsw
ms.assetid: def38214-2de9-4a26-93cb-e2f34d8dd6ef
ms.date: 12/05/2018
ms.keywords: WsRemoveCustomHeader, WsRemoveCustomHeader function [Web Services for Windows], webservices/WsRemoveCustomHeader, wsw.wsremovecustomheader
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
 - WsRemoveCustomHeader
 - webservices/WsRemoveCustomHeader
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
 - WsRemoveCustomHeader
---

# WsRemoveCustomHeader function


## -description

Removes a custom header from the message.
            
This function is designed to handle types of headers that appear once in the message and are targeted at the ultimate receiver. Headers targeted with a role other than ultimate receiver are ignored.

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object with the header  to be removed.  

The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b>.

### -param headerName [in]

A pointer to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> object that references the "local name" of the header element to be  removed.

### -param headerNs [in]

A pointer to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> object that references the namespace of the header element to be removed.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to serialize the header.

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

If a header of the given type exists in the message it is removed.  If the header does not exist, the function takes no action and completes successfully.