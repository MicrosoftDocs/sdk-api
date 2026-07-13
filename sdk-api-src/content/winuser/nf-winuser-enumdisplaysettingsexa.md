---
UID: NF:winuser.EnumDisplaySettingsExA
title: EnumDisplaySettingsExA function (winuser.h)
description: The EnumDisplaySettingsEx function retrieves information about one of the graphics modes for a display device. To retrieve information for all the graphics modes for a display device, make a series of calls to this function. (ANSI)
helpviewer_keywords: ["EDS_RAWMODE", "EDS_ROTATEDMODE", "ENUM_CURRENT_SETTINGS", "ENUM_REGISTRY_SETTINGS", "EnumDisplaySettingsExA", "winuser/EnumDisplaySettingsExA"]
old-location: gdi\enumdisplaysettingsex.htm
tech.root: gdi
ms.assetid: 99794fb1-7ba3-4864-bf6a-e3a514fa7917
ms.date: 12/05/2018
ms.keywords: EDS_RAWMODE, EDS_ROTATEDMODE, ENUM_CURRENT_SETTINGS, ENUM_REGISTRY_SETTINGS, EnumDisplaySettingsEx, EnumDisplaySettingsEx function [Windows GDI], EnumDisplaySettingsExA, EnumDisplaySettingsExW, _win32_EnumDisplaySettingsEx, gdi.enumdisplaysettingsex, winuser/EnumDisplaySettingsEx, winuser/EnumDisplaySettingsExA, winuser/EnumDisplaySettingsExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDisplaySettingsExW (Unicode) and EnumDisplaySettingsExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumDisplaySettingsExA
 - winuser/EnumDisplaySettingsExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-sysparams-l1-1-0.dll
api_name:
 - EnumDisplaySettingsEx
 - EnumDisplaySettingsExA
 - EnumDisplaySettingsExW
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# EnumDisplaySettingsExA function


## -description

The <b>EnumDisplaySettingsEx</b> function retrieves information about one of the graphics modes for a display device. To retrieve information for all the graphics modes for a display device, make a series of calls to this function.

This function differs from <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a> in that there is a <i>dwFlags</i> parameter.
<div class="alert"><b>Note</b>  Apps that you design to target Windows 8 and later can no longer query or set display modes that are less than 32 bits per pixel (bpp); these operations will fail. These apps have a <a href="/windows/desktop/Win7AppQual/compatibility---application-manifest">compatibility manifest</a> that targets Windows 8. Windows 8 still supports 8-bit and 16-bit color modes for desktop apps that were built without a Windows 8 manifest; Windows 8 emulates these modes but still runs in 32-bit color mode.</div><div> </div>

## -parameters

### -param lpszDeviceName [in]

A pointer to a null-terminated string that specifies the display device about which graphics mode the function will obtain information.

This parameter is either <b>NULL</b> or a <a href="/windows/desktop/api/wingdi/ns-wingdi-display_devicea">DISPLAY_DEVICE</a>.<b>DeviceName</b> returned from <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a>. A <b>NULL</b> value specifies the current display device on the computer that the calling thread is running on.

### -param iModeNum [in]

Indicates the type of information to be retrieved. This value can be a graphics mode index or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENUM_CURRENT_SETTINGS"></a><a id="enum_current_settings"></a><dl>
<dt><b>ENUM_CURRENT_SETTINGS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the current settings for the display device.

</td>
</tr>
<tr>
<td width="40%"><a id="ENUM_REGISTRY_SETTINGS"></a><a id="enum_registry_settings"></a><dl>
<dt><b>ENUM_REGISTRY_SETTINGS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the settings for the display device that are currently stored in the registry.

</td>
</tr>
</table>
 

Graphics mode indexes start at zero. To obtain information for all of a display device's graphics modes, make a series of calls to <b>EnumDisplaySettingsEx</b>, as follows: Set <i>iModeNum</i> to zero for the first call, and increment <i>iModeNum</i> by one for each subsequent call. Continue calling the function until the return value is zero.

When you call <b>EnumDisplaySettingsEx</b> with <i>iModeNum</i> set to zero, the operating system initializes and caches information about the display device. When you call <b>EnumDisplaySettingsEx</b> with <i>iModeNum</i> set to a nonzero value, the function returns the information that was cached the last time the function was called with <i>iModeNum</i> set to zero.

### -param lpDevMode [out]

A pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure into which the function stores information about the specified graphics mode. Before calling <b>EnumDisplaySettingsEx</b>, set the <b>dmSize</b> member to <b>sizeof</b> (<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>), and set the <b>dmDriverExtra</b> member to indicate the size, in bytes, of the additional space available to receive private driver data.

The <b>EnumDisplaySettingsEx</b> function will populate the <b>dmFields</b> member of the <b>lpDevMode</b> and one or more other members of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. To determine which members were set by the call to <b>EnumDisplaySettingsEx</b>, inspect the <i>dmFields</i> bitmask. Some of the fields typically populated by this function include:

<ul>
<li><b>dmBitsPerPel</b></li>
<li><b>dmPelsWidth</b></li>
<li><b>dmPelsHeight</b></li>
<li><b>dmDisplayFlags</b></li>
<li><b>dmDisplayFrequency</b></li>
<li><b>dmPosition</b></li>
<li><b>dmDisplayOrientation</b></li>
</ul>

### -param dwFlags [in]

This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EDS_RAWMODE"></a><a id="eds_rawmode"></a><dl>
<dt><b>EDS_RAWMODE</b></dt>
</dl>
</td>
<td width="60%">
If set, the function will return all graphics modes reported by the adapter driver, regardless of monitor capabilities. Otherwise, it will only return modes that are compatible with current monitors.

</td>
</tr>
<tr>
<td width="40%"><a id="EDS_ROTATEDMODE_"></a><a id="eds_rotatedmode_"></a><dl>
<dt><b>EDS_ROTATEDMODE </b></dt>
</dl>
</td>
<td width="60%">
If set, the function will return graphics modes in all orientations. Otherwise, it will only return modes that have the same orientation as the one currently set for the requested display.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The function fails if <i>iModeNum</i> is greater than the index of the display device's last graphics mode. As noted in the description of the <i>iModeNum</i> parameter, you can use this behavior to enumerate all of a display device's graphics modes.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output given is always in terms of physical pixels, and is not related to the calling context.





> [!NOTE]
> The winuser.h header defines EnumDisplaySettingsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a>



<a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsexa">ChangeDisplaySettingsEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-display_devicea">DISPLAY_DEVICE</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a>
