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

# _GetAppTrackerDataFlags enumeration


## -description


Controls what data is returned from calls to the <a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a> interface.


## -enum-fields




### -field GATD_INCLUDE_PROCESS_EXE_NAME

Include the name of the process's executable image in the <a href="https://msdn.microsoft.com/2402aca6-4992-4c6e-a6ff-b4cc50c57dde">ApplicationProcessSummary</a> structure. If set, it is the caller's responsibility to free the memory allocated for this string.


### -field GATD_INCLUDE_LIBRARY_APPS

Include COM+ library applications in the tracking data. By default, these are excluded.


### -field GATD_INCLUDE_SWC

Include Services Without Components contexts in the tracking data. By default, these are excluded.


### -field GATD_INCLUDE_CLASS_NAME

Include the class name in the <a href="https://msdn.microsoft.com/df752c4a-6a8d-4eac-b3dc-1647bf8a8e5a">ComponentSummary</a> structure. If set, it is the caller's responsibility to free the memory allocated for this string.


### -field GATD_INCLUDE_APPLICATION_NAME

Include the application name in the <a href="https://msdn.microsoft.com/3291eede-5318-4d97-a969-ce54381f30af">ApplicationSummary</a> and <a href="https://msdn.microsoft.com/df752c4a-6a8d-4eac-b3dc-1647bf8a8e5a">ComponentSummary</a> structures. If set, it is the caller's responsibility to free the memory allocated for this string.


## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

