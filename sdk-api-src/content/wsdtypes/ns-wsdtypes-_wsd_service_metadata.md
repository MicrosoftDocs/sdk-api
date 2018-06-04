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

# _WSD_SERVICE_METADATA structure


## -description


Provides metadata regarding a service hosted by a device.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://msdn.microsoft.com/fc9fed5c-8a5b-4960-836b-e083154b7d90">WSD_ENDPOINT_REFERENCE_LIST</a> structure that specifies the endpoints at which the service is available. 


### -field Types

Reference to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.


### -field ServiceId

The URI of the service. This URI must be valid when a <b>WSD_SERVICE_METADATA</b> structure is passed to <a href="https://msdn.microsoft.com/dc4cbed9-9ec4-4bbd-b1c9-89c4c11ff424">IWSDDeviceHost::SetMetadata</a>. Applications are responsible for URI validation.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

