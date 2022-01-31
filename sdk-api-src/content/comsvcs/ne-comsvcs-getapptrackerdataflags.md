---
UID: NE:comsvcs._GetAppTrackerDataFlags
title: GetAppTrackerDataFlags (comsvcs.h)
description: Controls what data is returned from calls to the IGetAppTrackerData interface.
helpviewer_keywords: ["GATD_INCLUDE_APPLICATION_NAME","GATD_INCLUDE_CLASS_NAME","GATD_INCLUDE_LIBRARY_APPS","GATD_INCLUDE_PROCESS_EXE_NAME","GATD_INCLUDE_SWC","GetAppTrackerDataFlags","GetAppTrackerDataFlags enumeration [COM+]","comsvcs/GATD_INCLUDE_APPLICATION_NAME","comsvcs/GATD_INCLUDE_CLASS_NAME","comsvcs/GATD_INCLUDE_LIBRARY_APPS","comsvcs/GATD_INCLUDE_PROCESS_EXE_NAME","comsvcs/GATD_INCLUDE_SWC","comsvcs/GetAppTrackerDataFlags","cos.getapptrackerdataflags"]
old-location: cos\getapptrackerdataflags.htm
tech.root: cos
ms.assetid: 7af61221-e876-4b1c-b416-a92817ad7025
ms.date: 12/05/2018
ms.keywords: GATD_INCLUDE_APPLICATION_NAME, GATD_INCLUDE_CLASS_NAME, GATD_INCLUDE_LIBRARY_APPS, GATD_INCLUDE_PROCESS_EXE_NAME, GATD_INCLUDE_SWC, GetAppTrackerDataFlags, GetAppTrackerDataFlags enumeration [COM+], comsvcs/GATD_INCLUDE_APPLICATION_NAME, comsvcs/GATD_INCLUDE_CLASS_NAME, comsvcs/GATD_INCLUDE_LIBRARY_APPS, comsvcs/GATD_INCLUDE_PROCESS_EXE_NAME, comsvcs/GATD_INCLUDE_SWC, comsvcs/GetAppTrackerDataFlags, cos.getapptrackerdataflags
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
targetos: Windows
req.typenames: GetAppTrackerDataFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GetAppTrackerDataFlags
 - comsvcs/_GetAppTrackerDataFlags
 - GetAppTrackerDataFlags
 - comsvcs/GetAppTrackerDataFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - GetAppTrackerDataFlags
---

# GetAppTrackerDataFlags enumeration


## -description

Controls what data is returned from calls to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a> interface.

## -enum-fields

### -field GATD_INCLUDE_PROCESS_EXE_NAME:0x1

Include the name of the process's executable image in the <a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationprocesssummary">ApplicationProcessSummary</a> structure. If set, it is the caller's responsibility to free the memory allocated for this string.

### -field GATD_INCLUDE_LIBRARY_APPS:0x2

Include COM+ library applications in the tracking data. By default, these are excluded.

### -field GATD_INCLUDE_SWC:0x4

Include Services Without Components contexts in the tracking data. By default, these are excluded.

### -field GATD_INCLUDE_CLASS_NAME:0x8

Include the class name in the <a href="/windows/desktop/api/comsvcs/ns-comsvcs-componentsummary">ComponentSummary</a> structure. If set, it is the caller's responsibility to free the memory allocated for this string.

### -field GATD_INCLUDE_APPLICATION_NAME:0x10

Include the application name in the <a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationsummary">ApplicationSummary</a> and <a href="/windows/desktop/api/comsvcs/ns-comsvcs-componentsummary">ComponentSummary</a> structures. If set, it is the caller's responsibility to free the memory allocated for this string.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>
