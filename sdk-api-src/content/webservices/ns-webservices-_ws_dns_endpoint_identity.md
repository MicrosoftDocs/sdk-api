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

# _WS_DNS_ENDPOINT_IDENTITY structure


## -description



                    Type for specifying an endpoint identity represented by a DNS name.
            


## -struct-fields




### -field identity


                    The base type from which this type and all other endpoint identity types derive.
                


### -field dns


                    The DNS name of the endpoint that is represented by this endpoint identity.
                    The acceptable forms of the name are as defined by <a href="http://go.microsoft.com/fwlink/p/?linkid=139702">RFC 1035</a>.
                    In particular, they include both a simple machine name as well as a fully qualified domain name (FQDN).
                

