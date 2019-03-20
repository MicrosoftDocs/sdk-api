---
UID: NE:webservices.__unnamed_enum_39
title: WS_MESSAGE_STATE (webservices.h)
author: windows-sdk-content
description: The different states that a message can be in.
old-location: wsw\ws_message_state.htm
tech.root: wsw
ms.assetid: 2c5ddedd-b0b4-4c26-a5c0-a5851f0408de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_MESSAGE_STATE, WS_MESSAGE_STATE enumeration [Web Services for Windows], WS_MESSAGE_STATE_DONE, WS_MESSAGE_STATE_EMPTY, WS_MESSAGE_STATE_INITIALIZED, WS_MESSAGE_STATE_READING, WS_MESSAGE_STATE_WRITING, webservices/WS_MESSAGE_STATE, webservices/WS_MESSAGE_STATE_DONE, webservices/WS_MESSAGE_STATE_EMPTY, webservices/WS_MESSAGE_STATE_INITIALIZED, webservices/WS_MESSAGE_STATE_READING, webservices/WS_MESSAGE_STATE_WRITING, wsw.ws_message_state
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
 - WS_MESSAGE_STATE
product: Windows
targetos: Windows
req.typenames: WS_MESSAGE_STATE
req.redist: 
---

# WS_MESSAGE_STATE enumeration


## -description


The different states that a message can be in.
            


## -enum-fields




### -field WS_MESSAGE_STATE_EMPTY

The initial state after a message has been created.
                    In this state, there is no content in the message, and
                    neither the header nor the body can be accessed.
                


### -field WS_MESSAGE_STATE_INITIALIZED

The message headers have been initialized, and
                    can be accessed, but the body cannot be accessed.  This state
                    is used to build up all the headers prior to writing/sending them.
                


### -field WS_MESSAGE_STATE_READING

The body of the message is being read, for example
                    when a message is received.
                    In this state, the headers can be accessed, and the body can
                    be read (see <a href="https://msdn.microsoft.com/43ceeb1e-aeb2-4482-90f0-d7f6013b239f">WsReadBody</a> or
                    <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_BODY_READER</a>).
                


### -field WS_MESSAGE_STATE_WRITING

The body of the message is being written, for example
                    when a message is being sent.
                    In this state, the headers can be accessed, and the body can
                    be written (see <a href="https://msdn.microsoft.com/70ff43f5-6f1a-4bbb-aa39-6fb9476e6a37">WsWriteBody</a> or
                    <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_BODY_WRITER</a>).
                


### -field WS_MESSAGE_STATE_DONE

The message body has been read or written (the end of the
                    body has been read or written).  The headers can still be accessed.
                


## -remarks



A message object transitions through a set of states as it
                is being received or sent (or read or written).
            

The following are the state transitions while writing or sending:
            

<img alt="" src="./images/MessageSendStates.png"/>
The following are the state transitions while reading or receiving:
            

<img alt="" src="./images/MessageReceiveStates.png"/>
Note that in the above diagrams, only valid transitions are
                shown.
            



