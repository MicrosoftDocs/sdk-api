---
UID: NF:webservices.WsResetChannel
title: WsResetChannel function (webservices.h)
description: Reset a channel so it can be reused.
helpviewer_keywords: ["WsResetChannel","WsResetChannel function [Web Services for Windows]","webservices/WsResetChannel","wsw.wsresetchannel"]
old-location: wsw\wsresetchannel.htm
tech.root: wsw
ms.assetid: 7aca8ae0-44a0-4ec7-87e8-bec9bd17d04b
ms.date: 12/05/2018
ms.keywords: WsResetChannel, WsResetChannel function [Web Services for Windows], webservices/WsResetChannel, wsw.wsresetchannel
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
 - WsResetChannel
 - webservices/WsResetChannel
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
 - WsResetChannel
---

# WsResetChannel function


## -description

Reset a channel so it can be reused.

## -parameters

### -param channel [in]

The channel to reset.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The channel was in an inappropriate state.
                

</td>
</tr>
</table>

## -remarks

Reusing a channel instead of creating one from scratch may improve performance.
            

This function is only valid when the channel is in the either the
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE_CREATED</a> or <b>WS_CHANNEL_STATE_CLOSED</b> state.
            

If called correctly, this function will not fail (for example, due to lack of system resources).