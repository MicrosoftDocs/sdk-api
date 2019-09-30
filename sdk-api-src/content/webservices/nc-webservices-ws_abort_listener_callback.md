---
UID: NC:webservices.WS_ABORT_LISTENER_CALLBACK
title: WS_ABORT_LISTENER_CALLBACK (webservices.h)
author: windows-sdk-content
description: Handles the WsAbortListener call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_abort_listener_callback.htm
tech.root: wsw
ms.assetid: 6105641e-72de-4826-a54d-23e877f0e6d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_ABORT_LISTENER_CALLBACK, WS_ABORT_LISTENER_CALLBACK callback, WS_ABORT_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_ABORT_LISTENER_CALLBACK, wsw.ws_abort_listener_callback
ms.topic: callback
f1_keywords: 
 - "webservices/WS_ABORT_LISTENER_CALLBACK"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_ABORT_LISTENER_CALLBACK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WS_ABORT_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsabortlistener">WsAbortListener</a> call
                for a <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nc-webservices-ws_create_listener_callback">WS_CREATE_LISTENER_CALLBACK</a>.
                


### -param *error [in, optional]

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
The listener was in an inappropriate state.
                

</td>
</tr>
</table>
 




## -remarks



See <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsabortlistener">WsAbortListener</a> for information about the contract
                of this API.
            



