---
UID: NE:comsvcs._GetAppTrackerDataFlags
title: GetAppTrackerDataFlags (comsvcs.h)
author: windows-sdk-content
description: Controls what data is returned from calls to the IGetAppTrackerData interface.
old-location: cos\getapptrackerdataflags.htm
tech.root: cossdk
ms.assetid: 7af61221-e876-4b1c-b416-a92817ad7025
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GATD_INCLUDE_APPLICATION_NAME, GATD_INCLUDE_CLASS_NAME, GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_PROCESS_EXE_NAME, GATD_INCLUDE_SWC, GetAppTrackerDataFlags, GetAppTrackerDataFlags enumeration [COM+], comsvcs/GATD_INCLUDE_APPLICATION_NAME, comsvcs/GATD_INCLUDE_CLASS_NAME, comsvcs/GATD_INCLUDE_LIBRARY_APPS, comsvcs/GATD_INCLUDE_PROCESS_EXE_NAME, comsvcs/GATD_INCLUDE_SWC, comsvcs/GetAppTrackerDataFlags, cos.getapptrackerdataflags
ms.topic: enum
f1_keywords: 
 - "comsvcs/GetAppTrackerDataFlags"
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
ms.custom: 19H1
---

# GetAppTrackerDataFlags enumeration


## -description


Controls what data is returned from calls to the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a> interface.


## -enum-fields




### -field GATD_INCLUDE_PROCESS_EXE_NAME

Include the name of the process's executable image in the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-_applicationprocesssummary">ApplicationProcessSummary</a> structure. If set, it is the caller's responsibility to free the memory allocated for this string.


### -field GATD_INCLUDE_LIBRARY_APPS

Include COM+ library applications in the tracking data. By default, these are excluded.


### -field GATD_INCLUDE_SWC

Include Services Without Components contexts in the tracking data. By default, these are excluded.


### -field GATD_INCLUDE_CLASS_NAME

Include the class name in the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-_componentsummary">ComponentSummary</a> structure. If set, it is the caller's responsibility to free the memory allocated for this string.


### -field GATD_INCLUDE_APPLICATION_NAME

Include the application name in the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-_applicationsummary">ApplicationSummary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-_componentsummary">ComponentSummary</a> structures. If set, it is the caller's responsibility to free the memory allocated for this string.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>
 

 

