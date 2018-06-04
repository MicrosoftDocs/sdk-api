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

# _RTM_PREF_INFO structure


## -description


The 
<b>RTM_PREF_INFO</b> structure contains the information used when comparing any two routes. The value of the <b>Preference</b> member is given more weight than the value of the <b>Metric</b> member.


## -struct-fields




### -field Metric

Specifies a metric. The metric is specific to a particular routing protocol.


### -field Preference

Specifies a preference. The preference is determined by the router policy.


## -remarks



Preference is more important than metric. The metric is only  checked if the preferences are equal.




## -see-also




<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>
 

 

