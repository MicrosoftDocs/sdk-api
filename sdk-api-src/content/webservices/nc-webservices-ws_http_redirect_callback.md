---
UID: NC:webservices.WS_HTTP_REDIRECT_CALLBACK
title: WS_HTTP_REDIRECT_CALLBACK (webservices.h)
author: windows-sdk-content
description: Invoked when a message is about to be automatically redirected to another service utilizing HTTP auto redirect functionality as described in RFC2616.
old-location: wsw\ws_http_redirect_callback.htm
tech.root: wsw
ms.assetid: 14bd68f9-1b0d-4667-823a-afb159d7dc80
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_HTTP_REDIRECT_CALLBACK, WS_HTTP_REDIRECT_CALLBACK callback, WS_HTTP_REDIRECT_CALLBACK callback function [Web Services for Windows], webservices/WS_HTTP_REDIRECT_CALLBACK, wsw.ws_http_redirect_callback
ms.topic: callback
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
 - WS_HTTP_REDIRECT_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_HTTP_REDIRECT_CALLBACK callback function


## -description


Invoked when a message is about to be automatically 
                redirected to another service utilizing HTTP auto redirect functionality 
                as described in RFC2616. If the redirection should not be allowed, this 
                callback should return S_FALSE or an error value. Otherwise the auto 
                HTTP redirection will proceed. 
            


## -parameters




### -param *state [in]

The 'state' as specified as part of <a href="https://msdn.microsoft.com/en-us/library/Dd401919(v=VS.85).aspx">WS_HTTP_REDIRECT_CALLBACK_CONTEXT</a> 'state' field.
                


### -param *originalUrl [in]

The original endpoint URL that the message was sent to.
                


### -param *newUrl [in]

The endpoint URL that the message is about to be forwarded to.
                


## -returns



This callback function does not return a value.




## -remarks



The parameters supplied during this callback are valid only for the 
                duration of the callback.
            

The callback implementation should avoid lengthy computation or 
                lengthy blocking calls so that it can return to the caller quickly.
            



