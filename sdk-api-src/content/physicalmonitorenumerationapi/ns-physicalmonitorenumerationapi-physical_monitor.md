---
UID: NS:physicalmonitorenumerationapi._PHYSICAL_MONITOR
title: PHYSICAL_MONITOR (physicalmonitorenumerationapi.h)
author: windows-sdk-content
description: Contains a handle and text description corresponding to a physical monitor.
old-location: monitor\physical_monitor.htm
tech.root: Monitor
ms.assetid: 58eb4999-37d9-472d-aa26-38b19a2287b2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPPHYSICAL_MONITOR, LPPHYSICAL_MONITOR, LPPHYSICAL_MONITOR structure pointer [Monitor Configuration], PHYSICAL_MONITOR, PHYSICAL_MONITOR structure [Monitor Configuration], monitor.physical_monitor, physicalmonitorenumerationapi/LPPHYSICAL_MONITOR, physicalmonitorenumerationapi/PHYSICAL_MONITOR"
ms.topic: struct
req.header: physicalmonitorenumerationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PhysicalMonitorEnumerationAPI.h
api_name:
 - PHYSICAL_MONITOR
product: Windows
targetos: Windows
req.typenames: PHYSICAL_MONITOR, *LPPHYSICAL_MONITOR
req.redist: 
---

# PHYSICAL_MONITOR structure


## -description


Contains a handle and text description corresponding to a physical monitor.
        


## -struct-fields




### -field hPhysicalMonitor

Handle to the physical monitor.
          


### -field szPhysicalMonitorDescription

Text description of the physical monitor.
          


## -remarks



A physical monitor description is always an array of 128 characters.




## -see-also




<a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a>



<a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/4aca3a00-d2c6-42a6-9143-72e42c1d33bb">Monitor Configuration Structures</a>
 

 

