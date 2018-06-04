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

# _WSD_RESOLVE_MATCH structure


## -description


Represents a ResolveMatch message.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies the matching endpoint. 


### -field Types

Reference to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.


### -field Scopes

Reference to a <a href="https://msdn.microsoft.com/3415fef0-dbf4-4ece-bad0-6cd6831404db">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.


### -field XAddrs

Reference to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that contains a list of WS-Discovery XAddrs.


### -field MetadataVersion

The metadata version of this message.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/0eaa4348-968e-4b45-9509-8b15476edaa1">ResolveMatches Message</a>



<a href="https://msdn.microsoft.com/f969f249-6c1e-4c0c-8da6-ec7069b06e20">WSD_RESOLVE</a>



<a href="https://msdn.microsoft.com/a6094069-af17-4921-b2c3-4ec89cbbb6f6">WSD_RESOLVE_MATCHES</a>
 

 

