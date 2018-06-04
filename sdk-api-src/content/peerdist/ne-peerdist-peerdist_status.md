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

# PEERDIST_STATUS enumeration


## -description


The <b>PEERDIST_STATUS</b> enumeration defines the possible status values of the Peer Distribution service.


## -enum-fields




### -field PEERDIST_STATUS_DISABLED

The service is disabled by Group Policy or according to configuration parameters.


### -field PEERDIST_STATUS_UNAVAILABLE

The service is not ready to process the request.


### -field PEERDIST_STATUS_AVAILABLE

The Peer Distribution service  is available and ready to process  requests.


## -see-also




<a href="https://msdn.microsoft.com/1ab188cc-db79-49b2-977f-0b8fccf7f274">PeerDistGetStatus</a>
 

 

