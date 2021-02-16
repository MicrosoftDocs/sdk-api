---
UID: NS:webservices._WS_PROXY_MESSAGE_CALLBACK_CONTEXT
title: WS_PROXY_MESSAGE_CALLBACK_CONTEXT (webservices.h)
description: Specifies the callback function and state for an application that wishes to associate or inspect headers in an input or an output message respectively.
helpviewer_keywords: ["WS_PROXY_MESSAGE_CALLBACK_CONTEXT","WS_PROXY_MESSAGE_CALLBACK_CONTEXT structure [Web Services for Windows]","webservices/WS_PROXY_MESSAGE_CALLBACK_CONTEXT","wsw.ws_proxy_message_callback_context"]
old-location: wsw\ws_proxy_message_callback_context.htm
tech.root: wsw
ms.assetid: 1dfde962-7475-430a-b586-1684a173908f
ms.date: 12/05/2018
ms.keywords: WS_PROXY_MESSAGE_CALLBACK_CONTEXT, WS_PROXY_MESSAGE_CALLBACK_CONTEXT structure [Web Services for Windows], webservices/WS_PROXY_MESSAGE_CALLBACK_CONTEXT, wsw.ws_proxy_message_callback_context
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
req.typenames: WS_PROXY_MESSAGE_CALLBACK_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_PROXY_MESSAGE_CALLBACK_CONTEXT
 - webservices/_WS_PROXY_MESSAGE_CALLBACK_CONTEXT
 - WS_PROXY_MESSAGE_CALLBACK_CONTEXT
 - webservices/WS_PROXY_MESSAGE_CALLBACK_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_PROXY_MESSAGE_CALLBACK_CONTEXT
---

# WS_PROXY_MESSAGE_CALLBACK_CONTEXT structure


## -description

Specifies the callback function and state for an application that wishes
                to associate or inspect headers in an input or an output message respectively.
            

See also, <a href="/windows/desktop/api/webservices/ne-webservices-ws_call_property_id">WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT</a> and  
                <b>WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT</b>.

## -struct-fields

### -field callback

application specific callback for handling the message.

### -field state

Application specific state that would be made available to the callback upon its invocation.