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

# LOG_LEVEL enumeration


## -description


Represents the severity of the log event passed to the 
    <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> callback function.


## -enum-fields




### -field LOG_INFORMATION

The event is informational.


### -field LOG_WARNING

The event is reporting a failure that might have happened, but it is uncertain whether a failure really did 
      occur.


### -field LOG_ERROR

The event affects a single component, but other components are not affected and the integrity of the rest 
      of the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> is not compromised.


### -field LOG_SEVERE

The event is reporting a severe failure that affects multiple components, or the integrity of the entire 
      system is compromised or believed to be compromised.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a>
 

 

