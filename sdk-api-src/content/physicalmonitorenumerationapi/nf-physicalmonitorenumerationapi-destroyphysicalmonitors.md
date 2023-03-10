---
UID: NF:physicalmonitorenumerationapi.DestroyPhysicalMonitors
title: DestroyPhysicalMonitors function (physicalmonitorenumerationapi.h)
description: Closes an array of physical monitor handles.
helpviewer_keywords: ["DestroyPhysicalMonitors","DestroyPhysicalMonitors function [Monitor Configuration]","monitor.destroyphysicalmonitors","physicalmonitorenumerationapi/DestroyPhysicalMonitors"]
old-location: monitor\destroyphysicalmonitors.htm
tech.root: Monitor
ms.assetid: ec9bbadf-93f3-4842-9bcc-e6a76f2f1ccf
ms.date: 12/05/2018
ms.keywords: DestroyPhysicalMonitors, DestroyPhysicalMonitors function [Monitor Configuration], monitor.destroyphysicalmonitors, physicalmonitorenumerationapi/DestroyPhysicalMonitors
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
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DestroyPhysicalMonitors
 - physicalmonitorenumerationapi/DestroyPhysicalMonitors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - DestroyPhysicalMonitors
---

# DestroyPhysicalMonitors function


## -description

Closes an array of physical monitor handles. Call this function to close an array of monitor handles obtained from the <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a> function.

## -parameters

### -param dwPhysicalMonitorArraySize [in]

Number of elements in the <i>pPhysicalMonitorArray</i> array.

### -param pPhysicalMonitorArray [in]

Pointer to an array of <a href="/windows/win32/api/physicalmonitorenumerationapi/ns-physicalmonitorenumerationapi-physical_monitor">PHYSICAL_MONITOR</a> structures.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-destroyphysicalmonitor">DestroyPhysicalMonitor Function</a>



<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>