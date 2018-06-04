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

# FAX_GROUP_STATUS_ENUM enumeration


## -description


The <b>FAX_GROUP_STATUS_ENUM</b> enumeration defines the status types for outbound routing groups.


## -enum-fields




### -field fgsALL_DEV_VALID

All the devices in the routing group are valid and available for sending outgoing faxes.


### -field fgsEMPTY

The routing group does not contain any devices.


### -field fgsALL_DEV_NOT_VALID

The routing group does not contain any available devices for sending faxes. (Devices can be "unavailable" when they are offline and when they do not exist.)


### -field fgsSOME_DEV_NOT_VALID

The routing group contains some devices that are unavailable for sending faxes. (Devices can be "unavailable" when they are offline and when they do not exist.)


## -see-also




<a href="https://msdn.microsoft.com/e009411d-07d1-4be3-a050-eea78084953f">IFaxOutboundRoutingGroup::get_Status</a>
 

 

