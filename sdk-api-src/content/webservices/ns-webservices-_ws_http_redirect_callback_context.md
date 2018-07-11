---
UID: NS:webservices._WS_HTTP_REDIRECT_CALLBACK_CONTEXT
title: "_WS_HTTP_REDIRECT_CALLBACK_CONTEXT"
author: windows-sdk-content
description: Specifies the callback function and state for controlling the HTTP auto redirection behavior.
old-location: wsw\ws_http_redirect_callback_context.htm
old-project: wsw
ms.assetid: 2348fcdb-2f76-4a30-91c4-ed7d63012da1
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_HTTP_REDIRECT_CALLBACK_CONTEXT, WS_HTTP_REDIRECT_CALLBACK_CONTEXT structure [Web Services for Windows], _WS_HTTP_REDIRECT_CALLBACK_CONTEXT, webservices/WS_HTTP_REDIRECT_CALLBACK_CONTEXT, wsw.ws_http_redirect_callback_context
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_HTTP_REDIRECT_CALLBACK_CONTEXT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_HTTP_REDIRECT_CALLBACK_CONTEXT structure


## -description



                Specifies the callback function and state for controlling the HTTP auto redirection behavior.
            


                See also, <b>WS_HTTP_REDIRECT_CALLBACK_CONTEXT</b> 
                and <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_HTTP_REDIRECT_CALLBACK_CONTEXT</a>.
            


## -struct-fields




### -field callback


                    Application specific callback for controlling HTTP auto redirections.
                


### -field state


                    Application specific state that would be made available to the callback upon its invocation.
                

