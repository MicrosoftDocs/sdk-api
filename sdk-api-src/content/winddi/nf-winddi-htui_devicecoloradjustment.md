---
UID: NF:winddi.HTUI_DeviceColorAdjustment
title: HTUI_DeviceColorAdjustment function (winddi.h)
description: The HTUI_DeviceColorAdjustment function can be used by graphics device drivers to display a dialog box that allows a user to adjust a device's halftoning properties.
helpviewer_keywords: ["HTUI_DeviceColorAdjustment","HTUI_DeviceColorAdjustment function [Display Devices]","display.htui_devicecoloradjustment","gdifncs_4f705094-588c-47ce-ac45-f0d2744ce5d2.xml","winddi/HTUI_DeviceColorAdjustment"]
old-location: display\htui_devicecoloradjustment.htm
tech.root: display
ms.assetid: 063320e3-b103-4c9a-ae82-790e5b768dc9
ms.date: 12/05/2018
ms.keywords: HTUI_DeviceColorAdjustment, HTUI_DeviceColorAdjustment function [Display Devices], display.htui_devicecoloradjustment, gdifncs_4f705094-588c-47ce-ac45-f0d2744ce5d2.xml, winddi/HTUI_DeviceColorAdjustment
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HTUI_DeviceColorAdjustment
 - winddi/HTUI_DeviceColorAdjustment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - HTUI_DeviceColorAdjustment
---

# HTUI_DeviceColorAdjustment function


## -description

The <b>HTUI_DeviceColorAdjustment</b> function can be used by graphics device drivers to display a dialog box that allows a user to adjust a device's halftoning properties.

## -parameters

### -param pDeviceName [in, optional]

Caller-supplied pointer to a NULL-terminated string representing a displayable device name.

### -param pDevHTAdjData [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-devhtadjdata">DEVHTADJDATA</a> structure.

## -returns

The function returns the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Greater than 0</b></dt>
</dl>
</td>
<td width="60%">
The user chose the dialog box's <b>OK</b> button.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The user chose the dialog box's <b>Cancel</b> button.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Less than 0</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>

## -remarks

A graphics driver interface, such as a printer interface DLL, can call the <b>HTUI_DeviceColorAdjustment</b> function to display a dialog box that allows a user to view and modify the device's halftoning properties. Depending on member values specified for the <a href="/windows/desktop/api/winddi/ns-winddi-devhtadjdata">DEVHTADJDATA</a> structure, the function will either enable the dialog box for user modification or just display caller-specified default values. If user modification is allowed, the function returns the modified parameters to the caller (using the DEVHTAJDATA structure), so the driver can pass them to the device.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devhtadjdata">DEVHTADJDATA</a>