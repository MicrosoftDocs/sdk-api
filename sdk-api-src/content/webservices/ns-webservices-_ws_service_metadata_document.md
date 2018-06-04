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

# _WS_SERVICE_METADATA_DOCUMENT structure


## -description



                Specifies the individual documents that make up the service metadata.
            


## -struct-fields




### -field content


                    A <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a>* representing the specific  XML Schema, WSDL or a Policy document.
                    The service model expects this to be valid for the lifetime of the <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>.
                


### -field name


                    The name of the document which will be suffixed to the URL path on which this document is serviced for HTTP GET support
                    for metadata retrieval. Note that this can be set to <b>NULL</b> if the application is only using Ws-MetadataExchange 1.1 for servicing
                    metadata request.
                


                    See <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> service endpoint property to see how to enable HTTP GET support or
                    WS-MetadataExchange 1.1 for servicing metadata request.
                

