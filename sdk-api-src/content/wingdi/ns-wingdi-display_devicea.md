---
UID: NS:wingdi._DISPLAY_DEVICEA
title: DISPLAY_DEVICEA (wingdi.h)
description: The DISPLAY_DEVICE structure receives information about the display device specified by the iDevNum parameter of the EnumDisplayDevices function. (ANSI)
helpviewer_keywords: ["*LPDISPLAY_DEVICEA","*PDISPLAY_DEVICEA","DISPLAY_DEVICE","DISPLAY_DEVICE structure [Windows GDI]","DISPLAY_DEVICEA","DISPLAY_DEVICEW","PDISPLAY_DEVICE","PDISPLAY_DEVICE structure pointer [Windows GDI]","_DISPLAY_DEVICEA","_DISPLAY_DEVICEW","_win32_DISPLAY_DEVICE_str","gdi.display_device","wingdi/DISPLAY_DEVICE","wingdi/DISPLAY_DEVICEA","wingdi/DISPLAY_DEVICEW","wingdi/PDISPLAY_DEVICE"]
old-location: gdi\display_device.htm
tech.root: gdi
ms.assetid: 9a7813fe-358a-44eb-99da-c63f98d055c3
ms.date: 12/05/2018
ms.keywords: '*LPDISPLAY_DEVICEA, *PDISPLAY_DEVICEA, DISPLAY_DEVICE, DISPLAY_DEVICE structure [Windows GDI], DISPLAY_DEVICEA, DISPLAY_DEVICEW, PDISPLAY_DEVICE, PDISPLAY_DEVICE structure pointer [Windows GDI], _DISPLAY_DEVICEA, _DISPLAY_DEVICEW, _win32_DISPLAY_DEVICE_str, gdi.display_device, wingdi/DISPLAY_DEVICE, wingdi/DISPLAY_DEVICEA, wingdi/DISPLAY_DEVICEW, wingdi/PDISPLAY_DEVICE'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DISPLAY_DEVICEW (Unicode) and DISPLAY_DEVICEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DISPLAY_DEVICEA, *PDISPLAY_DEVICEA, *LPDISPLAY_DEVICEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DISPLAY_DEVICEA
 - wingdi/_DISPLAY_DEVICEA
 - PDISPLAY_DEVICEA
 - wingdi/PDISPLAY_DEVICEA
 - DISPLAY_DEVICEA
 - wingdi/DISPLAY_DEVICEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - DISPLAY_DEVICE
 - DISPLAY_DEVICEA
 - DISPLAY_DEVICEW
---

# DISPLAY_DEVICEA structure


## -description

The <b>DISPLAY_DEVICE</b> structure receives information about the display device specified by the <i>iDevNum</i> parameter of the <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a> function.

## -struct-fields

### -field cb

Size, in bytes, of the <b>DISPLAY_DEVICE</b> structure. This must be initialized prior to calling <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a>.

### -field DeviceName

An array of characters identifying the device name. This is either the adapter device or the monitor device.

### -field DeviceString

An array of characters containing the device context string. This is either a description of the display adapter or of the display monitor.

### -field StateFlags

Device state flags. It can be any reasonable combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DISPLAY_DEVICE_ACTIVE</td>
<td>DISPLAY_DEVICE_ACTIVE specifies whether a monitor is  presented as being "on" by the respective GDI view. <b>Windows Vista:</b> EnumDisplayDevices will only enumerate monitors that can be presented as being "on."

</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_MIRRORING_DRIVER</td>
<td>Represents a pseudo device used to mirror application drawing for remoting or other purposes. An invisible pseudo monitor is associated with this device. For example, NetMeeting uses it. Note that <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> (SM_MONITORS) only accounts for visible display monitors.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_MODESPRUNED</td>
<td>The device has more display modes than its output devices support.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_PRIMARY_DEVICE</td>
<td>The primary desktop is on the device. For a system with a single display card, this is always set. For a system with multiple display cards, only one device can have this set.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_REMOVABLE</td>
<td>The device is removable; it cannot be the primary display.</td>
</tr>
<tr>
<td>DISPLAY_DEVICE_VGA_COMPATIBLE</td>
<td>The device is VGA compatible.</td>
</tr>
</table>

### -field DeviceID

Not used.

### -field DeviceKey

Reserved.

## -remarks

The four string members are set based on the parameters passed to <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a>. If the <i>lpDevice</i> param is <b>NULL</b>, then DISPLAY_DEVICE is filled in with information about the display adapter(s). If it is a valid device name, then it is filled in with information about the monitor(s) for that device.





> [!NOTE]
> The wingdi.h header defines DISPLAY_DEVICE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/device-context-structures">Device Context Structures</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices
      </a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>
