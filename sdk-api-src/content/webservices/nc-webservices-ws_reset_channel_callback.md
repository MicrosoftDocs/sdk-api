---
UID: NC:webservices.WS_RESET_CHANNEL_CALLBACK
title: WS_RESET_CHANNEL_CALLBACK (webservices.h)
description: Handles the WsResetChannel call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_RESET_CHANNEL_CALLBACK","WS_RESET_CHANNEL_CALLBACK callback","WS_RESET_CHANNEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_RESET_CHANNEL_CALLBACK","wsw.ws_reset_channel_callback"]
old-location: wsw\ws_reset_channel_callback.htm
tech.root: wsw
ms.assetid: 3f3b4995-72ca-4e93-87de-89996f9c43cb
ms.date: 12/05/2018
ms.keywords: WS_RESET_CHANNEL_CALLBACK, WS_RESET_CHANNEL_CALLBACK callback, WS_RESET_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_RESET_CHANNEL_CALLBACK, wsw.ws_reset_channel_callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_RESET_CHANNEL_CALLBACK
 - webservices/WS_RESET_CHANNEL_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_RESET_CHANNEL_CALLBACK
---

# WS_RESET_CHANNEL_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsresetchannel">WsResetChannel</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a>.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

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

See <a href="/windows/desktop/api/webservices/nf-webservices-wsresetchannel">WsResetChannel</a> for information about the contract
                of this API.
