---
UID: NE:webservices.WS_TRANSFER_MODE
title: WS_TRANSFER_MODE
author: windows-sdk-content
description: Whether messages that are sent or received are streamed or buffered.
old-location: wsw\ws_transfer_mode.htm
tech.root: wsw
ms.assetid: 6153bef6-f37f-4bc6-b1c5-5fbedd6bd234
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_BUFFERED_TRANSFER_MODE, WS_STREAMED_INPUT_TRANSFER_MODE, WS_STREAMED_OUTPUT_TRANSFER_MODE, WS_STREAMED_TRANSFER_MODE, WS_TRANSFER_MODE, WS_TRANSFER_MODE enumeration [Web Services for Windows], webservices/WS_BUFFERED_TRANSFER_MODE, webservices/WS_STREAMED_INPUT_TRANSFER_MODE, webservices/WS_STREAMED_OUTPUT_TRANSFER_MODE, webservices/WS_STREAMED_TRANSFER_MODE, webservices/WS_TRANSFER_MODE, wsw.ws_transfer_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - WS_TRANSFER_MODE
product: Windows
targetos: Windows
req.typenames: WS_TRANSFER_MODE
req.redist: 
---

# WS_TRANSFER_MODE enumeration


## -description


Whether messages that are sent or received are streamed or buffered.
            


## -enum-fields




### -field WS_STREAMED_INPUT_TRANSFER_MODE

Setting this flag means messages are delivered in chunks.  The start of the message
                    (opening tag, headers, and opening body tag) will be returned to the application
                    when <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> completes.  It is up to the application to call
                    <a href="https://msdn.microsoft.com/fe70338d-d2bf-4126-96b2-30ef6ebfa74d">WsFillBody</a> before reading each chunk of the message body.  The end of
                    the message (closing body and envelope tags) will be read when <a href="https://msdn.microsoft.com/3112be44-f610-421f-a4ea-0f87fc383540">WsReadMessageEnd</a>is called.
                

Not setting this flag means the entire message is read and buffered
                    in memory before <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> indicates completion.
                


### -field WS_STREAMED_OUTPUT_TRANSFER_MODE

Setting this flag means messages are transmitted in chunks.  The start of the message (opening
                    envelope tag, headers, and opening body tag) will be transmitted when <a href="https://msdn.microsoft.com/43cc43a5-7853-4170-911d-e514ac722da5">WsWriteMessageStart</a>is called.  It is up to the application to call <a href="https://msdn.microsoft.com/f94c409b-94c0-4440-8587-74322777261f">WsFlushBody</a> after writing each chunk 
                    of the message body to cause the chunk to be transmitted.
                    Any remaining body data will be transmitted when <a href="https://msdn.microsoft.com/329193a7-932a-46d0-8e46-eef6bbdb8fa2">WsWriteMessageEnd</a> is called, along with
                    the end of the message (closing body and envelope tags).
                

Not setting this flag means the entire message is buffered in 
                    memory and is only transmitted once <a href="https://msdn.microsoft.com/329193a7-932a-46d0-8e46-eef6bbdb8fa2">WsWriteMessageEnd</a> is called.
                


### -field WS_BUFFERED_TRANSFER_MODE

Messages that are written or read are buffered.
                

This is equivalent to specifying neither
                    <a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_STREAMED_INPUT_TRANSFER_MODE</a> nor
                    <b>WS_STREAMED_OUTPUT_TRANSFER_MODE</b>.
                


### -field WS_STREAMED_TRANSFER_MODE

Messages that are written or read are streamed.
                

This is equivalent to specifying both
                    <a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_STREAMED_INPUT_TRANSFER_MODE</a> and
                    <b>WS_STREAMED_OUTPUT_TRANSFER_MODE</b>.
                


## -remarks



This value is specified for a channel using the 
                <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_TRANSFER_MODE</a> channel property.
            

The streaming programming model can be used regardless of which 
                transfer mode is used.  In the case where streaming is not used, the calls
                to the calls to <a href="https://msdn.microsoft.com/fe70338d-d2bf-4126-96b2-30ef6ebfa74d">WsFillBody</a> and <a href="https://msdn.microsoft.com/f94c409b-94c0-4440-8587-74322777261f">WsFlushBody</a> are NOPs.
            



