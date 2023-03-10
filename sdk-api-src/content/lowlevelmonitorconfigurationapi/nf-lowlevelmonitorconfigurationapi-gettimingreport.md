---
UID: NF:lowlevelmonitorconfigurationapi.GetTimingReport
title: GetTimingReport function (lowlevelmonitorconfigurationapi.h)
description: Retrieves a monitor's horizontal and vertical synchronization frequencies.
helpviewer_keywords: ["GetTimingReport","GetTimingReport function [Monitor Configuration]","lowlevelmonitorconfigurationapi/GetTimingReport","monitor.gettimingreport"]
old-location: monitor\gettimingreport.htm
tech.root: Monitor
ms.assetid: 17b5a7e4-936f-451f-b586-032f94a99be5
ms.date: 12/05/2018
ms.keywords: GetTimingReport, GetTimingReport function [Monitor Configuration], lowlevelmonitorconfigurationapi/GetTimingReport, monitor.gettimingreport
req.header: lowlevelmonitorconfigurationapi.h
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
 - GetTimingReport
 - lowlevelmonitorconfigurationapi/GetTimingReport
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
 - GetTimingReport
---

# GetTimingReport function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves a monitor's horizontal and vertical synchronization frequencies.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param pmtrMonitorTimingReport [out]

Pointer to an <a href="/windows/win32/api/lowlevelmonitorconfigurationapi/ns-lowlevelmonitorconfigurationapi-mc_timing_report">MC_TIMING_REPORT</a> structure that receives the timing information.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function corresponds to the "Get Timing Report &amp; Timing Message" command from the Display Data Channel Command Interface (DDC/CI) standard. For more information about the timing information, refer to the DDC/CI standard.
      

This function takes about 50 milliseconds to return.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>