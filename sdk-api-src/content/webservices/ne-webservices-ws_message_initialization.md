---
UID: NE:webservices.__unnamed_enum_40
title: WS_MESSAGE_INITIALIZATION
author: windows-sdk-content
description: Specifies what headers the WsInitializeMessageshould add to the message.
old-location: wsw\ws_message_initialization.htm
tech.root: wsw
ms.assetid: f4a674c1-4017-49c8-aa9a-68f1d2b84378
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_BLANK_MESSAGE, WS_DUPLICATE_MESSAGE, WS_FAULT_MESSAGE, WS_MESSAGE_INITIALIZATION, WS_MESSAGE_INITIALIZATION enumeration [Web Services for Windows], WS_REPLY_MESSAGE, WS_REQUEST_MESSAGE, webservices/WS_BLANK_MESSAGE, webservices/WS_DUPLICATE_MESSAGE, webservices/WS_FAULT_MESSAGE, webservices/WS_MESSAGE_INITIALIZATION, webservices/WS_REPLY_MESSAGE, webservices/WS_REQUEST_MESSAGE, wsw.ws_message_initialization
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_MESSAGE_INITIALIZATION
product: Windows
targetos: Windows
req.typenames: WS_MESSAGE_INITIALIZATION
req.redist: 
---

# WS_MESSAGE_INITIALIZATION enumeration


## -description


Specifies what headers the
                <a href="https://msdn.microsoft.com/26eafc5f-6636-4f96-a037-7935cdac5900">WsInitializeMessage</a>should add to the message.
            


## -enum-fields




### -field WS_BLANK_MESSAGE

The headers of the message are empty.
                


### -field WS_DUPLICATE_MESSAGE

The headers are initialized to be the same as the source message's headers.
                


### -field WS_REQUEST_MESSAGE

If using <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_0_9</a> or <b>WS_ADDRESSING_VERSION_1_0</b>,
                    then a unique message ID is set as the MessageID header of the message.  
                    No other headers are added in the message.
                


### -field WS_REPLY_MESSAGE

The ReplyTo header of the source message (an <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a>)
                    is used to address the message.  The MessageID header of the source
                    message is used to add a RelatesTo header to the message.  If the message
                    will contain a fault reply, then <a href="https://msdn.microsoft.com/f4a674c1-4017-49c8-aa9a-68f1d2b84378">WS_FAULT_MESSAGE</a> should be
                    used instead.
                


### -field WS_FAULT_MESSAGE

The FaultTo or ReplyTo header of the source message (an <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a>)
                    is used to address the message.  The MessageID header of the source message
                    is used to add a RelatesTo header to the message.  This should only be
                    used when the contents of the message will contain a fault.
                

