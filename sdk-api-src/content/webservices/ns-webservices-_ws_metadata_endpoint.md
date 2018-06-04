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

# _WS_METADATA_ENDPOINT structure


## -description



                Information about a single endpoint that was
                read from metadata documents.
            


## -struct-fields




### -field endpointAddress


                    The address of the endpoint.
                


### -field endpointPolicy


                    An opaque handle representing the policy of the endpoint.  
                    This handle is good until the metadata object
                    is freed or reset.
                


### -field portName


                    The WSDL port name of the endpoint, if available.
                


### -field serviceName


                    The WSDL service name of the endpoint, if available.
                


### -field serviceNs


                    The WSDL service namespace of the endpoint, if available.
                


### -field bindingName


                    The WSDL binding name of the endpoint, if available.
                


### -field bindingNs


                    The WSDL binding namespace of the endpoint, if available.
                


### -field portTypeName


                    The WSDL portType name of the endpoint, if available.
                


### -field portTypeNs


                    The WSDL portType namespace of the endpoint, if available.
                

