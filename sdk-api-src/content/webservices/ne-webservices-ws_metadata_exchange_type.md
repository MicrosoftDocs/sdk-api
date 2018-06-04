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

# WS_METADATA_EXCHANGE_TYPE enumeration


## -description




## -enum-fields




### -field WS_METADATA_EXCHANGE_TYPE_NONE


                    Disables WS-MetadataExchange/HTTP GET servicing on the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>.  
                    This is the default value of  <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> property.
                


### -field WS_METADATA_EXCHANGE_TYPE_MEX


                    Enables servicing of WS-MetadataExchange 1.1 request servicing on the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>.
                


### -field WS_METADATA_EXCHANGE_TYPE_HTTP_GET


                    Enables servicing of HTTP GET request servicing on the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a> for metadata 
                    retrieval.
                

