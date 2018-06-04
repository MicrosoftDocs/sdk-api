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

# _WS_SERVICE_ENDPOINT structure


## -description



                Represents an individual endpoint on a service host. The properties on the endpoint
                are used to specify the address, binding and contract. 
            


## -struct-fields




### -field address


                    The URL address on which the endpoint is going to listen. 
                


### -field channelBinding


                    The binding for the channel/listener.
                


### -field channelType


                    The <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">type of channel</a> being hosted by the endpoint.
                


### -field securityDescription


                    A description of the security required for this channel. This can be <b>NULL</b> if no security is required.
                


### -field contract


                    The contract of the endpoint.
                


### -field authorizationCallback


                    Authorization callback for the service endpoint.
                


### -field properties


                    An array of properties to configure the service endpoint.
                


### -field propertyCount


                    Number of elements in the WS_SERVICE_ENDPOINT_PROPERTY array.
                


### -field channelProperties

                    Channel properties associated with the endpoint. An application should be careful in modifying default values. For example, modifying send/receive timeouts may result in unexpected behavior and cause the client to fail.


