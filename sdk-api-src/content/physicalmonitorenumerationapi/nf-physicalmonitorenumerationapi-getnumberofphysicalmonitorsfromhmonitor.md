---
UID: NF:physicalmonitorenumerationapi.GetNumberOfPhysicalMonitorsFromHMONITOR
title: GetNumberOfPhysicalMonitorsFromHMONITOR function (physicalmonitorenumerationapi.h)
description: Retrieves the number of physical monitors associated with an HMONITOR monitor handle.
helpviewer_keywords: ["GetNumberOfPhysicalMonitorsFromHMONITOR","GetNumberOfPhysicalMonitorsFromHMONITOR function [Monitor Configuration]","monitor.getnumberofphysicalmonitorsfromhmonitor","physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromHMONITOR"]
old-location: monitor\getnumberofphysicalmonitorsfromhmonitor.htm
tech.root: Monitor
ms.assetid: c4cc3012-10ae-4435-8d81-e0a9eb62b55c
ms.date: 12/05/2018
ms.keywords: GetNumberOfPhysicalMonitorsFromHMONITOR, GetNumberOfPhysicalMonitorsFromHMONITOR function [Monitor Configuration], monitor.getnumberofphysicalmonitorsfromhmonitor, physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromHMONITOR
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
 - GetNumberOfPhysicalMonitorsFromHMONITOR
 - physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromHMONITOR
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
 - GetNumberOfPhysicalMonitorsFromHMONITOR
---

# GetNumberOfPhysicalMonitorsFromHMONITOR function


## -description

Retrieves the number of physical monitors associated with an <b>HMONITOR</b> monitor handle. Call this function before calling <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a>.

## -parameters

### -param hMonitor [in]

A monitor handle. Monitor handles are returned by several Multiple Display Monitor functions, including <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> and <a href="/windows/desktop/api/winuser/nf-winuser-monitorfromwindow">MonitorFromWindow</a>, which are part of the graphics device interface (GDI).

### -param pdwNumberOfPhysicalMonitors [out]

Receives the number of physical monitors associated with the monitor handle.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a>



<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>