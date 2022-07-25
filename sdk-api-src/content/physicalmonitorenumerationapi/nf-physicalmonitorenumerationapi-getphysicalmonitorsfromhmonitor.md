---
UID: NF:physicalmonitorenumerationapi.GetPhysicalMonitorsFromHMONITOR
title: GetPhysicalMonitorsFromHMONITOR function (physicalmonitorenumerationapi.h)
description: Retrieves the physical monitors associated with an HMONITOR monitor handle.
helpviewer_keywords: ["GetPhysicalMonitorsFromHMONITOR","GetPhysicalMonitorsFromHMONITOR function [Monitor Configuration]","monitor.getphysicalmonitorsfromhmonitor","physicalmonitorenumerationapi/GetPhysicalMonitorsFromHMONITOR"]
old-location: monitor\getphysicalmonitorsfromhmonitor.htm
tech.root: Monitor
ms.assetid: f2ac8a6a-3be9-4155-ad13-c256b96da792
ms.date: 12/05/2018
ms.keywords: GetPhysicalMonitorsFromHMONITOR, GetPhysicalMonitorsFromHMONITOR function [Monitor Configuration], monitor.getphysicalmonitorsfromhmonitor, physicalmonitorenumerationapi/GetPhysicalMonitorsFromHMONITOR
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
 - GetPhysicalMonitorsFromHMONITOR
 - physicalmonitorenumerationapi/GetPhysicalMonitorsFromHMONITOR
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
 - GetPhysicalMonitorsFromHMONITOR
---

# GetPhysicalMonitorsFromHMONITOR function


## -description

Retrieves the physical monitors associated with an <b>HMONITOR</b> monitor handle.

## -parameters

### -param hMonitor [in]

A monitor handle. Monitor handles are returned by several Multiple Display Monitor functions, including <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors">EnumDisplayMonitors</a> and <a href="/windows/desktop/api/winuser/nf-winuser-monitorfromwindow">MonitorFromWindow</a>, which are part of the graphics device interface (GDI).

### -param dwPhysicalMonitorArraySize [in]

Number of elements in <i>pPhysicalMonitorArray</i>. To get the required size of the array, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor">GetNumberOfPhysicalMonitorsFromHMONITOR</a>.

### -param pPhysicalMonitorArray [out]

Pointer to an array of <a href="/windows/win32/api/physicalmonitorenumerationapi/ns-physicalmonitorenumerationapi-physical_monitor">PHYSICAL_MONITOR</a> structures. The caller must allocate the array.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A single <b>HMONITOR</b> handle can be associated with more than one physical monitor. This function returns a handle and a text description for each physical monitor.
      

When you are done using the monitor handles, close them by passing the <i>pPhysicalMonitorArray</i> array to the <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-destroyphysicalmonitors">DestroyPhysicalMonitors</a> function.
      


#### Examples


```cpp

HMONITOR hMonitor = NULL;
DWORD cPhysicalMonitors;
LPPHYSICAL_MONITOR pPhysicalMonitors = NULL;

// Get the monitor handle.
hMonitor = MonitorFromWindow(hWnd, MONITOR_DEFAULTTOPRIMARY);

// Get the number of physical monitors.
BOOL bSuccess = GetNumberOfPhysicalMonitorsFromHMONITOR(
  hMonitor, 
  &cPhysicalMonitors
   );

if (bSuccess)
{
    // Allocate the array of PHYSICAL_MONITOR structures.
    pPhysicalMonitors = (LPPHYSICAL_MONITOR)malloc(
        cPhysicalMonitors* sizeof(PHYSICAL_MONITOR));

    if (pPhysicalMonitors != NULL)
    {
        // Get the array.
        bSuccess = GetPhysicalMonitorsFromHMONITOR(
            hMonitor, cPhysicalMonitors, pPhysicalMonitors);

       // Use the monitor handles (not shown).

        // Close the monitor handles.
        bSuccess = DestroyPhysicalMonitors(
            cPhysicalMonitors, 
            pPhysicalMonitors);

        // Free the array.
        free(pPhysicalMonitors);
    }
}

```

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
