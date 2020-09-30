---
UID: NF:webservices.WsRemoveMappedHeader
title: WsRemoveMappedHeader function (webservices.h)
description: Removes all instances of a mapped header from the message.
helpviewer_keywords: ["WsRemoveMappedHeader","WsRemoveMappedHeader function [Web Services for Windows]","webservices/WsRemoveMappedHeader","wsw.wsremovemappedheader"]
old-location: wsw\wsremovemappedheader.htm
tech.root: wsw
ms.assetid: aa662c92-4fb4-47af-b260-a3dedf4c6c9a
ms.date: 12/05/2018
ms.keywords: WsRemoveMappedHeader, WsRemoveMappedHeader function [Web Services for Windows], webservices/WsRemoveMappedHeader, wsw.wsremovemappedheader
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
 - WsRemoveMappedHeader
 - webservices/WsRemoveMappedHeader
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
 - WsRemoveMappedHeader
---

# WsRemoveMappedHeader function


## -description

Removes all instances of a mapped header from the message.

## -parameters

### -param message [in]

The message to set the header in.
                

The message can be in any state but <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a>.

### -param headerName [in]

The name of the mapped header to remove.

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

A message may contain additional transport-specific information that is
                not part of the message envelope.  This transport-specific information
                can be exposed programmatically as headers of the Message object.
                This function is used to remove mapped headers from the message object.
                This can be used by a custom channel implementation to remove mapped headers
                prior to sending the message.