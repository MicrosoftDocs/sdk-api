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

# FWPM_VSWITCH_EVENT_SUBSCRIPTION0_ structure


## -description


The <b>FWPM_VSWITCH_EVENT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a vSwitch event.


## -struct-fields




### -field flags

Type: <b>UINT32</b>

This member is reserved for future use.


### -field sessionKey

Type: <b>GUID</b>

Identifies the session which created the subscription.


## -remarks



<b>FWPM_VSWITCH_EVENT_SUBSCRIPTION0</b> is a specific implementation of FWPM_VSWITCH_EVENT_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/1264a58d-81e1-4877-915d-6ed3d7d15512">FwpmvSwitchEventSubscribe0</a>
 

 

