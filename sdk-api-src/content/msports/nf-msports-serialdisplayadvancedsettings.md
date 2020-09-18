---
UID: NF:msports.SerialDisplayAdvancedSettings
title: SerialDisplayAdvancedSettings function (msports.h)
description: SerialDisplayAdvancedSettings displays the system-supplied advanced settings dialog box for a specified COM port device.
helpviewer_keywords: ["SerialDisplayAdvancedSettings","SerialDisplayAdvancedSettings function [Serial Ports]","comdb_6cace01c-3c22-4699-938d-9fb180d79f12.xml","msports/SerialDisplayAdvancedSettings","serports.serialdisplayadvancedsettings"]
old-location: serports\serialdisplayadvancedsettings.htm
tech.root: serports
ms.assetid: 185c66e9-0c72-4aca-a99c-54995384e26e
ms.date: 12/05/2018
ms.keywords: SerialDisplayAdvancedSettings, SerialDisplayAdvancedSettings function [Serial Ports], comdb_6cace01c-3c22-4699-938d-9fb180d79f12.xml, msports/SerialDisplayAdvancedSettings, serports.serialdisplayadvancedsettings
req.header: msports.h
req.include-header: Msports.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: Msports.lib
req.dll: Msports.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SerialDisplayAdvancedSettings
 - msports/SerialDisplayAdvancedSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msports.dll
api_name:
 - SerialDisplayAdvancedSettings
---

# SerialDisplayAdvancedSettings function


## -description

<b>SerialDisplayAdvancedSettings</b> displays the system-supplied advanced settings dialog box for a specified COM port device.

## -parameters

### -param ParentHwnd [in]

Handle to the parent window for the advanced settings dialog box.

### -param DeviceInfoSet [in]

Specifies the device information set that includes the device instance specified by <i>DeviceInfoData</i>.

### -param DeviceInfoData [in]

Pointer to the device instance in the specified device information set. The routine displays the advanced settings dialog box for this device.

## -returns

<b>SerialDisplayAdvancedSettings</b> returns one of the following status values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The advanced settings dialog box was successfully displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following occurred: The specified device information set is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not open the specified device's hardware registry key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The name of the port is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not display the dialog box.

</td>
</tr>
</table>

## -remarks

<b>SerialDisplayAdvancedSettings</b> displays the system-supplied advanced settings dialog box for a specified device. If you supply a custom dialog box, this routine displays it; otherwise, the routine displays the default dialog box.

<b>SerialDisplayAdvancedSettings</b> runs in user mode.

For more information, see <a href="/previous-versions/ff546508(v=vs.85)">Installing an Advanced Properties Page for a COM Port</a>.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff546956(v=vs.85)">PPORT_ADVANCED_DIALOG</a>