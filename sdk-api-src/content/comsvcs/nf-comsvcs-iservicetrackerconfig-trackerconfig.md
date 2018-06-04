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

# IServiceTrackerConfig::TrackerConfig


## -description


Configures the tracker property for the enclosed work.



## -parameters




### -param trackerConfig [in]

A value from the <a href="https://msdn.microsoft.com/48f01634-9802-4824-b251-ccb6e71aa099">CSC_TrackerConfig</a> enumeration.


### -param szTrackerAppName [in]

The application identifier under which tracker information is reported.


### -param szTrackerCtxName [in]

The context name under which tracker information is reported.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



Because no component is associated with this tracker property, tracker activity is reported as arising from a component with the name specified by <i>szTrackerAppName</i>.





## -see-also




<a href="https://msdn.microsoft.com/342713d0-be5e-4d47-85ba-b18673a17fb5">IServiceTrackerConfig</a>
 

 

