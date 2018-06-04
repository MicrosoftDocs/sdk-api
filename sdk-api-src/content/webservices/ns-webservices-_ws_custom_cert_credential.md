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

# _WS_CUSTOM_CERT_CREDENTIAL structure


## -description


The type for specifying a certificate credential that is to be
supplied by a callback to the application.  This callback is invoked
to get the certificate during <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a> on the client
side and during <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a> on the server side.  It is
always invoked <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">short</a>.
            


## -struct-fields




### -field credential


The base type from which this type and all other certificate credential types derive.
                


### -field getCertCallback


The Callback to get the certificate.
                


### -field getCertCallbackState


The state to be passed when invoking the callback.
                


### -field certIssuerListNotificationCallback

 


### -field certIssuerListNotificationCallbackState

 



