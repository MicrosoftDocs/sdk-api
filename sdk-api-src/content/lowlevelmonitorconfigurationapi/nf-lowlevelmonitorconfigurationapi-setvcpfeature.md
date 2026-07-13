---
UID: NF:lowlevelmonitorconfigurationapi.SetVCPFeature
title: SetVCPFeature function (lowlevelmonitorconfigurationapi.h)
description: Sets the value of a Virtual Control Panel (VCP) code for a monitor.
helpviewer_keywords: ["SetVCPFeature","SetVCPFeature function [Monitor Configuration]","lowlevelmonitorconfigurationapi/SetVCPFeature","monitor.setvcpfeature"]
old-location: monitor\setvcpfeature.htm
tech.root: Monitor
ms.assetid: 145c393e-dce0-4d50-94c2-61ba580c3d83
ms.date: 12/05/2018
ms.keywords: SetVCPFeature, SetVCPFeature function [Monitor Configuration], lowlevelmonitorconfigurationapi/SetVCPFeature, monitor.setvcpfeature
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
 - SetVCPFeature
 - lowlevelmonitorconfigurationapi/SetVCPFeature
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
 - SetVCPFeature
---

# SetVCPFeature function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Sets the value of a Virtual Control Panel (VCP) code for a monitor.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param bVCPCode [in]

VCP code to set. The VCP codes are defined in the VESA Monitor Control Command Set (MCCS) standard, version 1.0 and 2.0. This parameter must specify a continuous or non-continuous VCP, or a vendor-specific code. It should not be a table control code.

### -param dwNewValue [in]

Value of the VCP code.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function corresponds to the "Set VCP Feature" command from the Display Data Channel Command Interface (DDC/CI) standard.

This function takes about 50 milliseconds to return.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
