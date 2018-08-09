---
UID: NC:webservices.WS_PROXY_MESSAGE_CALLBACK
title: WS_PROXY_MESSAGE_CALLBACK
author: windows-sdk-content
description: Invoked when the headers of the input message are about to be sent, or when output message headers are just received.
old-location: wsw\ws_proxy_message_callback.htm
old-project: wsw
ms.assetid: 5590ef4f-38a5-4aeb-9e77-803abb7ef6a7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_PROXY_MESSAGE_CALLBACK, WS_PROXY_MESSAGE_CALLBACK callback, WS_PROXY_MESSAGE_CALLBACK callback function [Web Services for Windows], webservices/WS_PROXY_MESSAGE_CALLBACK, wsw.ws_proxy_message_callback
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_PROXY_MESSAGE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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

The 'state' as specified as part of <a href="https://msdn.microsoft.com/1dfde962-7475-430a-b586-1684a173908f">WS_PROXY_MESSAGE_CALLBACK_CONTEXT</a> 'state' field.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See also, <a href="https://msdn.microsoft.com/1dfde962-7475-430a-b586-1684a173908f">WS_PROXY_MESSAGE_CALLBACK_CONTEXT</a>.
            



