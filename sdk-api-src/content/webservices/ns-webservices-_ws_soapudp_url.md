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

# _WS_SOAPUDP_URL structure


## -description



The URL subtype for specifying an soap.udp URL.
        


## -struct-fields




### -field url


The base type from which this URL subtype and all other URL subtypes derive. The <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> is <b>WS_URL_SOAPUDP_SCHEME_TYPE</b>.


### -field host


The host name.
            


### -field port


The port number.
            


### -field portAsString


The port number as string.
            


### -field path


The path.
            


### -field query


The query.
            


### -field fragment


The fragment.
            


## -remarks




                If used with the <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a> field, portAsString is a zero-length string if no port is specified in url.
            




## -see-also




<a href="https://msdn.microsoft.com/4a7cf425-40c6-4951-880e-b3a99076bb2b">WS_HTTPS_URL</a>



<a href="https://msdn.microsoft.com/36f4dda6-d46a-44cd-b4cd-597fa3298870">WS_HTTP_URL</a>



<a href="https://msdn.microsoft.com/62079e59-01c8-48fb-932a-ca01cc7b86ec">WS_NETTCP_URL</a>
 

 

