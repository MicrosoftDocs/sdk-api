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

# WS_CALL_PROPERTY_ID enumeration


## -description



                Optional parameters for configuring a call on a client side service operation.
            


## -enum-fields




### -field WS_CALL_PROPERTY_CHECK_MUST_UNDERSTAND


                    An application can suppress or enable must understand header processing 
                    on the proxy using this setting. This is <b>TRUE</b> by default.
                


### -field WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT

Enables an application to put headers into the input message for a given call. 




### -field WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT

Enables an application to extract headers from the output message for a given call. 




### -field WS_CALL_PROPERTY_CALL_ID


                    On a <a href="https://msdn.microsoft.com/788940a0-b1d9-45d7-a4b5-6f0926026c7d">service operation</a> an application can use the call id property to uniquely identify 
                    a service operation function all on a channel. This ID can be passed on to <a href="https://msdn.microsoft.com/709af94d-44ad-46af-8771-99d0aba5d77d">WsAbandonCall</a> along with the
                    service proxy to abandon the call.
                


                    For more information about abandoning calls see <a href="https://msdn.microsoft.com/9d6e2441-91de-4108-b1c4-282fbca5fe7c">service operation</a>.
                

