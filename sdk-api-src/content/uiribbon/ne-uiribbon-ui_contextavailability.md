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

# UI_CONTEXTAVAILABILITY enumeration


## -description


Specifies values that identify the availability of a <a href="https://msdn.microsoft.com/1f57a8d7-97ac-4007-8a36-c6aec5b85e6c">contextual tab</a>.


## -enum-fields




### -field UI_CONTEXTAVAILABILITY_NOTAVAILABLE

A contextual tab is not available for the selected object.


### -field UI_CONTEXTAVAILABILITY_AVAILABLE

A contextual tab is available for the selected object. The tab is not the active tab.


### -field UI_CONTEXTAVAILABILITY_ACTIVE

A contextual tab is available for the selected object. The tab is the active tab.


## -remarks



A contextual tab  is displayed based on the <b>UI_CONTEXTAVAILABILITY</b> value in <a href="https://msdn.microsoft.com/d3cd551d-e71e-4b49-a8b6-f3cd25cf2535">UI_PKEY_ContextAvailable</a>.




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/d3cd551d-e71e-4b49-a8b6-f3cd25cf2535">UI_PKEY_ContextAvailable</a>
 

 

