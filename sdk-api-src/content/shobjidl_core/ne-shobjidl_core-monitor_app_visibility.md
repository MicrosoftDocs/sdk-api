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

# MONITOR_APP_VISIBILITY enumeration


## -description


Specifies whether a display is showing desktop windows instead of Windows Store apps.


## -enum-fields




### -field MAV_UNKNOWN

The display state is not known.


### -field MAV_NO_APP_VISIBLE

The display is showing desktop windows.


### -field MAV_APP_VISIBLE

The display is not showing desktop windows.


## -remarks



The <b>MONITOR_APP_VISIBILITY</b> enum is used by the <a href="https://msdn.microsoft.com/F03AEE1F-1156-4565-871E-4C8CB5C4EDCA">GetAppVisibilityOnMonitor</a> method.




## -see-also




<a href="https://msdn.microsoft.com/89E26D36-3536-45F5-9396-83CCFB26890B">IAppVisibility</a>
 

 

