---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
            

<img alt="" src="images/MessageSendStates.png"/>

                The following are the state transitions while reading or receiving:
            

<img alt="" src="images/MessageReceiveStates.png"/>

                Note that in the above diagrams, only valid transitions are
                shown.
            



