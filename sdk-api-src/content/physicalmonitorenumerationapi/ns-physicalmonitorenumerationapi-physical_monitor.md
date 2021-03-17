---
UID: NS:physicalmonitorenumerationapi._PHYSICAL_MONITOR
title: PHYSICAL_MONITOR (physicalmonitorenumerationapi.h)
description: Contains a handle and text description corresponding to a physical monitor.
helpviewer_keywords: ["*LPPHYSICAL_MONITOR","LPPHYSICAL_MONITOR","LPPHYSICAL_MONITOR structure pointer [Monitor Configuration]","PHYSICAL_MONITOR","PHYSICAL_MONITOR structure [Monitor Configuration]","monitor.physical_monitor","physicalmonitorenumerationapi/LPPHYSICAL_MONITOR","physicalmonitorenumerationapi/PHYSICAL_MONITOR"]
old-location: monitor\physical_monitor.htm
tech.root: Monitor
ms.assetid: 58eb4999-37d9-472d-aa26-38b19a2287b2
ms.date: 12/05/2018
ms.keywords: '*LPPHYSICAL_MONITOR, LPPHYSICAL_MONITOR, LPPHYSICAL_MONITOR structure pointer [Monitor Configuration], PHYSICAL_MONITOR, PHYSICAL_MONITOR structure [Monitor Configuration], monitor.physical_monitor, physicalmonitorenumerationapi/LPPHYSICAL_MONITOR, physicalmonitorenumerationapi/PHYSICAL_MONITOR'
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
targetos: Windows
req.typenames: PHYSICAL_MONITOR, *LPPHYSICAL_MONITOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PHYSICAL_MONITOR
 - physicalmonitorenumerationapi/_PHYSICAL_MONITOR
 - LPPHYSICAL_MONITOR
 - physicalmonitorenumerationapi/LPPHYSICAL_MONITOR
 - PHYSICAL_MONITOR
 - physicalmonitorenumerationapi/PHYSICAL_MONITOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PhysicalMonitorEnumerationAPI.h
api_name:
 - PHYSICAL_MONITOR
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

<a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a>



<a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>



<a href="/windows/desktop/Monitor/monitor-configuration-structures">Monitor Configuration Structures</a>