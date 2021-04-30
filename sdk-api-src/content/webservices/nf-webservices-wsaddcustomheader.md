---
UID: NF:webservices.WsAddCustomHeader
title: WsAddCustomHeader function (webservices.h)
description: Adds the specified application-defined header to the message.
helpviewer_keywords: ["WsAddCustomHeader","WsAddCustomHeader function [Web Services for Windows]","webservices/WsAddCustomHeader","wsw.wsaddcustomheader"]
old-location: wsw\wsaddcustomheader.htm
tech.root: wsw
ms.assetid: 4b95085a-e522-4ab2-b7c9-d332599c5598
ms.date: 12/05/2018
ms.keywords: WsAddCustomHeader, WsAddCustomHeader function [Web Services for Windows], webservices/WsAddCustomHeader, wsw.wsaddcustomheader
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
 - WsAddCustomHeader
 - webservices/WsAddCustomHeader
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
 - WsAddCustomHeader
---

# WsAddCustomHeader function


## -description

Adds the specified application-defined header to the <a href="/windows/desktop/wsw/message">message</a>.

## -parameters

### -param message [in]

The message to which to add the header.
                

The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b> (see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE</a> enumeration..

### -param headerDescription [in]

The <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> structure that describes the header.

### -param writeOption [in]

Whether the header element is required, and how the value is allocated.
                    For more information, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> enumeration.

### -param value [in, ref]

The header value to serialize.  For more information, see  the <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> enumeration.

### -param valueSize [in]

The size of the value being serialized, in bytes.

### -param headerAttributes [in]

The values of the SOAP attributes for the header.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
There are multiple instances of the same type of header present in the message.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

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

The <b>WsAddCustomHeader</b> function is designed handle types of headers that are targeted at 
                the final receiver.  Headers targeted at another receiver are ignored.
            

If you are replacing a header, call the <a href="/windows/desktop/api/webservices/nf-webservices-wsremovecustomheader">WsRemoveCustomHeader</a> function to remove 
                the existing instances of the header before calling <b>WsAddCustomHeader</b>.