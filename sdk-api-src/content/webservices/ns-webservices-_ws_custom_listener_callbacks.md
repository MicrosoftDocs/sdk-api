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

# _WS_CUSTOM_LISTENER_CALLBACKS structure


## -description



                A structure that is used to specify a set of callbacks 
                that form the implementation of a custom
                listener.
            


## -struct-fields




### -field createListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a>.
                    See <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a> for more information.
                


### -field freeListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/3a8a4cd3-d98e-467b-bbed-5cbd66f892ed">WsFreeListener</a>.
                    See <a href="https://msdn.microsoft.com/fd60ae42-5b3f-4482-b785-541f7379ab3e">WS_FREE_LISTENER_CALLBACK</a> for more information.
                


### -field resetListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/c23c8ad4-a193-42f2-9e4a-3e814b7bbdb2">WsResetListener</a>.
                    See <a href="https://msdn.microsoft.com/98a48403-5ac6-44c2-8a43-c81746390a0d">WS_RESET_LISTENER_CALLBACK</a> for more information.
                


### -field openListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>.
                    See <a href="https://msdn.microsoft.com/061111f5-a568-4a8a-9892-9c8a352556ef">WS_OPEN_LISTENER_CALLBACK</a> for more information.
                


### -field closeListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/6023595a-ac52-4619-a824-df49da887fc5">WsCloseListener</a>.
                    See <a href="https://msdn.microsoft.com/9a5d6b10-b4c8-41ba-9b69-4537e44416df">WS_CLOSE_LISTENER_CALLBACK</a> for more information.
                


### -field abortListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/894a325b-53ac-4f45-ac24-87ed3a40b03d">WsAbortListener</a>.
                    See <a href="https://msdn.microsoft.com/6105641e-72de-4826-a54d-23e877f0e6d9">WS_ABORT_LISTENER_CALLBACK</a> for more information.
                


### -field getListenerPropertyCallback


                    The callback that implements <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a>.
                    See <a href="https://msdn.microsoft.com/c2f79c5c-4a4f-4a45-ac70-432f818e7b46">WS_GET_LISTENER_PROPERTY_CALLBACK</a> for more information.
                


### -field setListenerPropertyCallback


                    The callback that implements <a href="https://msdn.microsoft.com/5c494651-3944-4424-8cd4-a6e14c239e80">WsSetListenerProperty</a>.
                    See <a href="https://msdn.microsoft.com/ed3cc3b3-eeb2-4f70-8e2f-8c25aadac4a9">WS_SET_LISTENER_PROPERTY_CALLBACK</a> for more information.
                


### -field createChannelForListenerCallback


                    The callback that implements <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                    See <a href="https://msdn.microsoft.com/e5644452-8f58-45de-8dc2-878bbb05fcf3">WS_CREATE_CHANNEL_FOR_LISTENER_CALLBACK</a> for more information.
                


### -field acceptChannelCallback


                    The callback that implements <a href="https://msdn.microsoft.com/e18e0005-89bd-435e-9a12-6602c3c638b7">WsAcceptChannel</a>.
                    See <a href="https://msdn.microsoft.com/2c7f36cf-ee7d-4de0-8599-ccfd066cca7e">WS_ACCEPT_CHANNEL_CALLBACK</a> for more information.
                


## -remarks




                This structure is specified when a listener is created using
                <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> 
                using <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_CALLBACKS</a>.
            


                Except where noted, each callback is responsible for validating all parameters and
                that the operation requested is acceptable given the current
                <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a>.
            



