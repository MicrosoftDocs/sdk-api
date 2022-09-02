---
UID: NF:lowlevelmonitorconfigurationapi.SaveCurrentSettings
title: SaveCurrentSettings function (lowlevelmonitorconfigurationapi.h)
description: Saves the current monitor settings to the display's nonvolatile storage. (SaveCurrentSettings)
helpviewer_keywords: ["SaveCurrentSettings","SaveCurrentSettings function [Monitor Configuration]","lowlevelmonitorconfigurationapi/SaveCurrentSettings","monitor.savecurrentsettings"]
old-location: monitor\savecurrentsettings.htm
tech.root: Monitor
ms.assetid: e5903e52-d04c-4ac3-9566-eb4f2559464b
ms.date: 12/05/2018
ms.keywords: SaveCurrentSettings, SaveCurrentSettings function [Monitor Configuration], lowlevelmonitorconfigurationapi/SaveCurrentSettings, monitor.savecurrentsettings
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
 - SaveCurrentSettings
 - lowlevelmonitorconfigurationapi/SaveCurrentSettings
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
 - SaveCurrentSettings
---

# SaveCurrentSettings function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Saves the current monitor settings to the display's nonvolatile storage.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function corresponds to the "Save Current Settings" function from the Display Data Channel Command Interface (DDC/CI) standard.
      

This function takes about 200 milliseconds to return.
      

This low-level function is identical to the high-level function <a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings">SaveCurrentMonitorSettings</a>.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
