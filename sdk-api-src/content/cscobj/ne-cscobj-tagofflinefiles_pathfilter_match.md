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

# tagOFFLINEFILES_PATHFILTER_MATCH enumeration


## -description


Specifies how closely an event must match a filter.


## -enum-fields




### -field OFFLINEFILES_PATHFILTER_SELF

Event must be an exact match for the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_CHILD

Event must be for an immediate child of the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_DESCENDENT

Event can be any descendant of the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_SELFORCHILD

Event must be an exact match or an immediate child of the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_SELFORDESCENDENT

Event must be an exact match or any descendant of the fully qualified UNC path associated with the filter.


## -see-also




<a href="https://msdn.microsoft.com/0b9d8339-3daa-4f0c-8a52-59e06b663163">IOfflineFilesEventsFilter::GetPathFilter</a>
 

 

