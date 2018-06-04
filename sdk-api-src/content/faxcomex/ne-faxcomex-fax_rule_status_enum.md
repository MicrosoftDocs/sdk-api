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

# FAX_RULE_STATUS_ENUM enumeration


## -description


The <b>FAX_RULE_STATUS_ENUM</b> enumeration defines the status types for outbound routing rules.


## -enum-fields




### -field frsVALID

The routing rule is valid and can be applied to outbound faxes.


### -field frsEMPTY_GROUP

The routing rule cannot be applied because the rule uses an outbound routing group for its destination and the group is empty.


### -field frsALL_GROUP_DEV_NOT_VALID

The routing rule cannot be applied because the rule uses an existing outbound routing group for its destination and the group does not contain devices that are valid for sending faxes.


### -field frsSOME_GROUP_DEV_NOT_VALID

The routing rule uses an existing outbound routing group for its destination but the group contains devices that are not valid for sending faxes.




This is a warning status. The rule can be applied to the valid devices in the routing group.



### -field frsBAD_DEVICE

The routing rule cannot be applied because the rule uses a single device for its destination and that device is not valid for sending faxes.


## -see-also




<a href="https://msdn.microsoft.com/5a880005-92a2-4809-b64c-b5af63382203">IFaxOutboundRoutingRule::get_Status</a>
 

 

