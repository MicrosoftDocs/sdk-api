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

# POWERBROADCAST_SETTING structure


## -description


Sent with a power setting event and contains data about the specific change. For more 
    information, see <a href="https://msdn.microsoft.com/840390ca-d32a-4cf3-9e75-66322c7cdee0">Registering for Power 
    Events</a> and <a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>.


## -struct-fields




### -field PowerSetting

Indicates the power setting for which this notification is being delivered. For more 
    info, see <a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>.


### -field DataLength

The size in bytes of the data in the  <i>Data</i> member.


### -field Data

The new value of the power setting. The type and possible values for this member depend on <i>PowerSettng.</i>


## -see-also




<a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>



<a href="https://msdn.microsoft.com/840390ca-d32a-4cf3-9e75-66322c7cdee0">Registering for Power Events</a>
 

 

