---
UID: NC:webservices.WS_MESSAGE_DONE_CALLBACK
title: WS_MESSAGE_DONE_CALLBACK
author: windows-sdk-content
description: Notifies the caller that the message has completed its use of either the WS_XML_READER structure that was supplied to WsReadEnvelopeStartfunction, or of the WS_XML_WRITER structure supplied to the WsWriteEnvelopeStart function.
old-location: wsw\ws_message_done_callback.htm
tech.root: wsw
ms.assetid: 59ab7cbe-dc66-4e74-bec9-ffb25173ff87
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_MESSAGE_DONE_CALLBACK, WS_MESSAGE_DONE_CALLBACK callback, WS_MESSAGE_DONE_CALLBACK callback function [Web Services for Windows], webservices/WS_MESSAGE_DONE_CALLBACK, wsw.ws_message_done_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
 - WS_MESSAGE_DONE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_MESSAGE_DONE_CALLBACK callback function


## -description


Notifies the caller that the message has completed its use of either the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> structure that was supplied to <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a>function, or of the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> structure supplied to the  <a href="https://msdn.microsoft.com/213fe780-82f2-4140-92f2-2665317a5cb6">WsWriteEnvelopeStart</a> function.


## -parameters




### -param *doneCallbackState [in]

A pointer to <b>state</b> information passed to the  <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a> or <a href="https://msdn.microsoft.com/213fe780-82f2-4140-92f2-2665317a5cb6">WsWriteEnvelopeStart</a> function.
                

This parameter can be used to specify a pointer to user-defined
                    data required by the callback.
                


## -returns



This callback function does not return a value.




## -remarks



This callback can be used as an indicator that the message object is no
                longer using the reader or writer.
            

The callback is specified when <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a> or
                <a href="https://msdn.microsoft.com/213fe780-82f2-4140-92f2-2665317a5cb6">WsWriteEnvelopeStart</a> is called.
            

The callback should assume that it is invoked as a 
                <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_SHORT_CALLBACK</a>, since it will be invoked on the same 
                thread that calls <a href="https://msdn.microsoft.com/50e08300-9445-4741-9298-bd80fc777041">WsFreeMessage</a> or <a href="https://msdn.microsoft.com/90a62cc8-a7e0-4451-8490-f6384bf3e7b6">WsResetMessage</a>.
            



