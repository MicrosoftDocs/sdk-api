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

# _RM_FILTER_TRIGGER enumeration


## -description


Describes the restart or shutdown actions for an application or service.


## -enum-fields




### -field RmFilterTriggerInvalid

An invalid filter trigger.


### -field RmFilterTriggerFile

Modifies the shutdown or restart actions for an application identified by its   executable filename.


### -field RmFilterTriggerProcess

Modifies the shutdown or restart actions for an application identified by a <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structure.


### -field RmFilterTriggerService

Modifies the shutdown or restart actions for a service identified by a service short name.


## -see-also




<a href="https://msdn.microsoft.com/b0fd12e4-20e3-48d1-a2db-c1e0334ed427">RM_FILTER_INFO</a>
 

 

