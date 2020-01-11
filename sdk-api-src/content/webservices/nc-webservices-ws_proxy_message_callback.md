---
UID: NC:webservices.WS_PROXY_MESSAGE_CALLBACK
title: WS_PROXY_MESSAGE_CALLBACK (webservices.h)
description: Invoked when the headers of the input message are about to be sent, or when output message headers are just received.
old-location: wsw\ws_proxy_message_callback.htm
tech.root: wsw
ms.assetid: 5590ef4f-38a5-4aeb-9e77-803abb7ef6a7
ms.date: 12/05/2018
ms.keywords: WS_PROXY_MESSAGE_CALLBACK, WS_PROXY_MESSAGE_CALLBACK callback, WS_PROXY_MESSAGE_CALLBACK callback function [Web Services for Windows], webservices/WS_PROXY_MESSAGE_CALLBACK, wsw.ws_proxy_message_callback
f1_keywords:
- webservices/WS_PROXY_MESSAGE_CALLBACK
dev_langs:
- c++
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
- WS_PROXY_MESSAGE_CALLBACK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WS_PROXY_MESSAGE_CALLBACK callback function


## -description


Invoked when the headers of the input message are 
                about to be sent, or when output message headers are just received. 
            


## -parameters




### -param *message [in]

The input or output message.
                


### -param *heap [in]

The heap associated with the call. This is the heap which is passed to call for which this 
                    callback is being called.
                


### -param *state [in]

The 'state' as specified as part of <a href="https://docs.microsoft.com/windows/win32/api/webservices/ns-webservices-ws_proxy_message_callback_context">WS_PROXY_MESSAGE_CALLBACK_CONTEXT</a> 'state' field.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See also, <a href="https://docs.microsoft.com/windows/win32/api/webservices/ns-webservices-ws_proxy_message_callback_context">WS_PROXY_MESSAGE_CALLBACK_CONTEXT</a>.
            



