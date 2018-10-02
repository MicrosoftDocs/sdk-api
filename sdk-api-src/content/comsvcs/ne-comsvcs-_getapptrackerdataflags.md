---
UID: NE:comsvcs._GetAppTrackerDataFlags
title: "_GetAppTrackerDataFlags"
author: windows-sdk-content
description: Controls what data is returned from calls to the IGetAppTrackerData interface.
old-location: cos\getapptrackerdataflags.htm
tech.root: cossdk
ms.assetid: 7af61221-e876-4b1c-b416-a92817ad7025
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GATD_INCLUDE_APPLICATION_NAME, GATD_INCLUDE_CLASS_NAME, GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_PROCESS_EXE_NAME, GATD_INCLUDE_SWC, GetAppTrackerDataFlags, GetAppTrackerDataFlags enumeration [COM+], _GetAppTrackerDataFlags, comsvcs/GATD_INCLUDE_APPLICATION_NAME, comsvcs/GATD_INCLUDE_CLASS_NAME, comsvcs/GATD_INCLUDE_LIBRARY_APPS, comsvcs/GATD_INCLUDE_PROCESS_EXE_NAME, comsvcs/GATD_INCLUDE_SWC, comsvcs/GetAppTrackerDataFlags, cos.getapptrackerdataflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - GetAppTrackerDataFlags
product: Windows
targetos: Windows
req.typenames: GetAppTrackerDataFlags
req.redist: 
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
 

 

