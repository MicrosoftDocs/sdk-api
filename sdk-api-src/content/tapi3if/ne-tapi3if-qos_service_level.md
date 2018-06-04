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

# QOS_SERVICE_LEVEL enumeration


## -description


The 
<b>QOS_SERVICE_LEVEL</b> enum is used by the 
<a href="https://msdn.microsoft.com/f1e6ef32-5706-4b1c-a1fa-a7be48fd6efd">ITBasicCallControl::SetQOS</a> method to indicate quality of service requirements for a call.


## -enum-fields




### -field QSL_NEEDED

Quality of service level required.


### -field QSL_IF_AVAILABLE

Quality of service level desired if available.


### -field QSL_BEST_EFFORT

Quality of service level desired is "best effort."


## -see-also




<a href="https://msdn.microsoft.com/f1e6ef32-5706-4b1c-a1fa-a7be48fd6efd">ITBasicCallControl::SetQOS</a>



<a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>
 

 

