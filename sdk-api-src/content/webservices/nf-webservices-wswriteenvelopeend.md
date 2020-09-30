---
UID: NF:webservices.WsWriteEnvelopeEnd
title: WsWriteEnvelopeEnd function (webservices.h)
description: Writes the closing elements of a message.
helpviewer_keywords: ["WsWriteEnvelopeEnd","WsWriteEnvelopeEnd function [Web Services for Windows]","webservices/WsWriteEnvelopeEnd","wsw.wswriteenvelopeend"]
old-location: wsw\wswriteenvelopeend.htm
tech.root: wsw
ms.assetid: 4d19d70d-76c5-42db-ae15-1e1ebf9c5aac
ms.date: 12/05/2018
ms.keywords: WsWriteEnvelopeEnd, WsWriteEnvelopeEnd function [Web Services for Windows], webservices/WsWriteEnvelopeEnd, wsw.wswriteenvelopeend
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
 - WsWriteEnvelopeEnd
 - webservices/WsWriteEnvelopeEnd
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
 - WsWriteEnvelopeEnd
---

# WsWriteEnvelopeEnd function


## -description

Writes the closing elements of a message.
            This function writes the end of the message including the element that closes the body
                tag and the envelope tag.
            Use this function when writing messages to destinations other  than channels.  With
                channels use <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessageend">WsWriteMessageEnd</a>

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object to write.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

To use this function the message state must be set to <b>WS_MESSAGE_STATE_WRITING</b>.  If called in the correct
                state the message will transition to <b>WS_MESSAGE_STATE_DONE</b> regardless
                of whether the function fails or not.