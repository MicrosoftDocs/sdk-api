---
UID: NS:webservices._WS_CUSTOM_CHANNEL_CALLBACKS
title: "_WS_CUSTOM_CHANNEL_CALLBACKS"
author: windows-sdk-content
description: A structure that is used to specify a set of callbacks that form the implementation of a custom channel.
old-location: wsw\ws_custom_channel_callbacks.htm
tech.root: wsw
ms.assetid: 8df774fd-7cfc-4006-84ad-b81737770b6e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_CUSTOM_CHANNEL_CALLBACKS, WS_CUSTOM_CHANNEL_CALLBACKS structure [Web Services for Windows], _WS_CUSTOM_CHANNEL_CALLBACKS, webservices/WS_CUSTOM_CHANNEL_CALLBACKS, wsw.ws_custom_channel_callbacks
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_CUSTOM_CHANNEL_CALLBACKS
product: Windows
targetos: Windows
req.typenames: WS_CUSTOM_CHANNEL_CALLBACKS
req.redist: 
---

# _WS_CUSTOM_CHANNEL_CALLBACKS structure


## -description


A structure that is used to specify a set of callbacks
                that form the implementation of a custom channel.
            


## -struct-fields




### -field createChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a>.
                    See <a href="https://msdn.microsoft.com/440114f9-2258-4c33-93cd-7185ccf36f76">WS_CREATE_CHANNEL_CALLBACK</a> for more information.
                


### -field freeChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">WsFreeChannel</a>.
                    See <a href="https://msdn.microsoft.com/f1781c50-824e-4b79-91b6-97e31581617a">WS_FREE_CHANNEL_CALLBACK</a> for more information.
                


### -field resetChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/7aca8ae0-44a0-4ec7-87e8-bec9bd17d04b">WsResetChannel</a>.
                    See <a href="https://msdn.microsoft.com/3f3b4995-72ca-4e93-87de-89996f9c43cb">WS_RESET_CHANNEL_CALLBACK</a> for more information.
                


### -field openChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a>.
                    See <a href="https://msdn.microsoft.com/5f36b4f1-37e4-48ed-a331-d4edc7d3413b">WS_OPEN_CHANNEL_CALLBACK</a> for more information.
                


### -field closeChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/e4928371-a172-4cc8-968b-12ae2ee2e0c6">WsCloseChannel</a>.
                    See <a href="https://msdn.microsoft.com/363ac4e0-5cfe-4c12-ad06-027ec2b735e6">WS_CLOSE_CHANNEL_CALLBACK</a> for more information.
                


### -field abortChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a>.
                    See <a href="https://msdn.microsoft.com/b2841065-5724-4fbb-92f0-b3b7ad1a6e26">WS_ABORT_CHANNEL_CALLBACK</a> for more information.
                


### -field getChannelPropertyCallback

The callback that implements <a href="https://msdn.microsoft.com/6f3440d2-90cc-4312-bb08-51f08b864cc7">WsGetChannelProperty</a>.
                    See <a href="https://msdn.microsoft.com/8fd503a9-6f8d-46c3-9338-c900b9b1d747">WS_GET_CHANNEL_PROPERTY_CALLBACK</a> for more information.
                


### -field setChannelPropertyCallback

The callback that implements <a href="https://msdn.microsoft.com/0bf3ec1b-c711-4c26-9c54-5d0184c89871">WsSetChannelProperty</a>.
                    See <a href="https://msdn.microsoft.com/8f7f90dd-0967-4caf-a781-5fc9c588238d">WS_SET_CHANNEL_PROPERTY_CALLBACK</a> for more information.
                


### -field writeMessageStartCallback

The callback that implements <a href="https://msdn.microsoft.com/43cc43a5-7853-4170-911d-e514ac722da5">WsWriteMessageStart</a>.
                    See <a href="https://msdn.microsoft.com/55a9a297-1a6e-41cf-a605-02c4cfef8ed0">WS_WRITE_MESSAGE_START_CALLBACK</a> for more information.
                


### -field writeMessageEndCallback

The callback that implements <a href="https://msdn.microsoft.com/329193a7-932a-46d0-8e46-eef6bbdb8fa2">WsWriteMessageEnd</a>.
                    See <a href="https://msdn.microsoft.com/308f4df8-6dc3-4b78-a066-3fc6da3155b9">WS_WRITE_MESSAGE_END_CALLBACK</a> for more information.
                


### -field readMessageStartCallback

The callback that implements <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a>.
                    See <a href="https://msdn.microsoft.com/e9c5d9df-2f96-472d-ba9d-ecb7ccac4a13">WS_READ_MESSAGE_START_CALLBACK</a> for more information.
                


### -field readMessageEndCallback

The callback that implements <a href="https://msdn.microsoft.com/3112be44-f610-421f-a4ea-0f87fc383540">WsReadMessageEnd</a>.
                    See <a href="https://msdn.microsoft.com/6e03b812-9022-4c17-b25d-e06cc8943a1b">WS_READ_MESSAGE_END_CALLBACK</a> for more information.
                


### -field abandonMessageCallback

The callback that implements <a href="https://msdn.microsoft.com/b8f5da50-d296-4550-8810-114d1f0e810b">WsAbandonMessage</a>.
                    See <a href="https://msdn.microsoft.com/494cfb49-c09e-4f51-85fd-5bb0f8d0a45d">WS_ABANDON_MESSAGE_CALLBACK</a> for more information.
                


### -field shutdownSessionChannelCallback

The callback that implements <a href="https://msdn.microsoft.com/db12b0b7-698e-4c74-b547-6c95d0c5fdb7">WsShutdownSessionChannel</a>.
                    See <a href="https://msdn.microsoft.com/7dba0ae5-5610-4b8f-bbe5-b89244779e2d">WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK</a> for more information.
                


## -remarks



This structure is specified when a channel is created using
                <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a> or <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>using <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_CALLBACKS</a>.
            

Except where noted, each callback is responsible for validating all parameters and
                that the operation requested is acceptable given the current
                <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE</a>.
            



