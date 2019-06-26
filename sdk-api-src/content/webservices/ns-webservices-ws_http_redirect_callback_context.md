---
UID: NS:webservices._WS_HTTP_REDIRECT_CALLBACK_CONTEXT
title: WS_HTTP_REDIRECT_CALLBACK_CONTEXT (webservices.h)
author: windows-sdk-content
description: Specifies the callback function and state for controlling the HTTP auto redirection behavior.
old-location: wsw\ws_http_redirect_callback_context.htm
tech.root: wsw
ms.assetid: 2348fcdb-2f76-4a30-91c4-ed7d63012da1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_HTTP_REDIRECT_CALLBACK_CONTEXT, WS_HTTP_REDIRECT_CALLBACK_CONTEXT structure [Web Services for Windows], webservices/WS_HTTP_REDIRECT_CALLBACK_CONTEXT, wsw.ws_http_redirect_callback_context
ms.topic: struct
f1_keywords: 
 - "webservices/WS_HTTP_REDIRECT_CALLBACK_CONTEXT"
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
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HTTP_REDIRECT_CALLBACK_CONTEXT
product: Windows
targetos: Windows
req.typenames: WS_HTTP_REDIRECT_CALLBACK_CONTEXT
req.redist: 
ms.custom: 19H1
---

# WS_HTTP_REDIRECT_CALLBACK_CONTEXT structure


## -description


Specifies the callback function and state for controlling the HTTP auto redirection behavior.
            

See also, <b>WS_HTTP_REDIRECT_CALLBACK_CONTEXT</b> 
                and <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_HTTP_REDIRECT_CALLBACK_CONTEXT</a>.
            


## -struct-fields




### -field callback

Application specific callback for controlling HTTP auto redirections.
                


### -field state

Application specific state that would be made available to the callback upon its invocation.
                

