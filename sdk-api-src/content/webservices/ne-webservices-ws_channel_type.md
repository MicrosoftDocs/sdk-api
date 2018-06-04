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

# WS_CHANNEL_TYPE enumeration


## -description



                Indicates the basic characteristics of the channel, such as whether it is
                sessionful, and what directions of communication are supported.
            


## -enum-fields




### -field WS_CHANNEL_TYPE_INPUT


                    Input channels support Receive operations.  They are used on the sender side.
                


                    The <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_UDP_CHANNEL_BINDING</a> supports this channel type
                    when used with <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                


### -field WS_CHANNEL_TYPE_OUTPUT


                    Output channels support Send operations.
                


                    This channel type is not currently supported by any channel bindings.
                


### -field WS_CHANNEL_TYPE_SESSION


                    Sessionful channels provide channel-level correlation of all messages sent or received.
                


                    This is a flag used to build <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_INPUT_SESSION</a>,
                    <b>WS_CHANNEL_TYPE_OUTPUT_SESSION</b>, and <b>WS_CHANNEL_TYPE_DUPLEX_SESSION</b>,
                    but cannot be used alone. 
                


### -field WS_CHANNEL_TYPE_INPUT_SESSION


                    An input channel that supports a session.
                


                    This channel type is not currently supported by any channel bindings.
                


### -field WS_CHANNEL_TYPE_OUTPUT_SESSION


                    An output channel that supports a session.
                


                    This channel type is not currently supported by any channel bindings.
                


### -field WS_CHANNEL_TYPE_DUPLEX


                    An input/output channel.
                


                    The <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_UDP_CHANNEL_BINDING</a> supports this channel type
                    when used with <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a>.
                


### -field WS_CHANNEL_TYPE_DUPLEX_SESSION


                    An input/output channel that supports a session.
                


                    The <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> supports this channel type when
                    used with <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a> or <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                


### -field WS_CHANNEL_TYPE_REQUEST


                    Request channels support Send followed by Receive.  They are used on the client 
                    side for channels that support request-reply operations.
                


                    The <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a> supports this channel type when
                    used with <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a>.
                


                    Note that request channels provide built-in correlation of request replies.
                    It is possible to do request-reply correlation on other channel types using the
                    addressing headers (RelatesTo and MessageID).
                


### -field WS_CHANNEL_TYPE_REPLY


                    Reply channels support Receive followed by Send.  They are used on the service
                    side for channels that support request-reply operations (for example, HTTP).
                


                    The <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a> supports this channel type when
                    used with <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                


                    Note that reply channels provide built-in correlation of request replies.
                    It is possible to do request-reply correlation on other channel types using the
                    addressing headers (RelatesTo and MessageID).
                

