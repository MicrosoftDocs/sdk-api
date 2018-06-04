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

# _PNRP_CLOUD_FLAGS enumeration


## -description


The <b>PNRP_CLOUD_FLAGS</b> enumeration specifies the validity of a cloud name.


## -enum-fields




### -field PNRP_CLOUD_NO_FLAGS

The cloud name is valid on the network.


### -field PNRP_CLOUD_NAME_LOCAL

The cloud name is not valid on other computers.


### -field PNRP_CLOUD_RESOLVE_ONLY

The cloud is configured to be resolve only.  Names cannot be published to the cloud from this computer.


### -field PNRP_CLOUD_FULL_PARTICIPANT

This machine is a full participant in the cloud, and can publish and resolve names.


## -see-also




<a href="https://msdn.microsoft.com/b3e1abf4-ff59-481d-b96e-f8916a47cd52">PNRP and WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/82af5a4f-1b29-405a-a200-1d723ea7693b">PNRPCLOUDINFO</a>
 

 

