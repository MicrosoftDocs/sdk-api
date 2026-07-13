---
UID: NF:winuser.ChangeDisplaySettingsExA
title: ChangeDisplaySettingsExA function (winuser.h)
description: The ChangeDisplaySettingsEx function changes the settings of the specified display device to the specified graphics mode. (ANSI)
helpviewer_keywords: ["CDS_DISABLE_UNSAFE_MODES", "CDS_ENABLE_UNSAFE_MODES", "CDS_FULLSCREEN", "CDS_GLOBAL", "CDS_NORESET", "CDS_RESET", "CDS_SET_PRIMARY", "CDS_TEST", "CDS_UPDATEREGISTRY", "CDS_VIDEOPARAMETERS", "ChangeDisplaySettingsExA", "winuser/ChangeDisplaySettingsExA"]
old-location: gdi\changedisplaysettingsex.htm
tech.root: gdi
ms.assetid: 1448e04c-1452-4eab-bda4-4d249cb67a24
ms.date: 12/05/2018
ms.keywords: CDS_DISABLE_UNSAFE_MODES, CDS_ENABLE_UNSAFE_MODES, CDS_FULLSCREEN, CDS_GLOBAL, CDS_NORESET, CDS_RESET, CDS_SET_PRIMARY, CDS_TEST, CDS_UPDATEREGISTRY, CDS_VIDEOPARAMETERS, ChangeDisplaySettingsEx, ChangeDisplaySettingsEx function [Windows GDI], ChangeDisplaySettingsExA, ChangeDisplaySettingsExW, _win32_ChangeDisplaySettingsEx, gdi.changedisplaysettingsex, winuser/ChangeDisplaySettingsEx, winuser/ChangeDisplaySettingsExA, winuser/ChangeDisplaySettingsExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ChangeDisplaySettingsExW (Unicode) and ChangeDisplaySettingsExA (ANSI)
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
 - ChangeDisplaySettingsExA
 - winuser/ChangeDisplaySettingsExA
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
 - ChangeDisplaySettingsEx
 - ChangeDisplaySettingsExA
 - ChangeDisplaySettingsExW
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# ChangeDisplaySettingsExA function


## -description

The <b>ChangeDisplaySettingsEx</b> function changes the settings of the specified display device to the specified graphics mode.
<div class="alert"><b>Note</b>  Apps that you design to target Windows 8 and later can no longer query or set display modes that are less than 32 bits per pixel (bpp); these operations will fail. These apps have a <a href="/windows/desktop/Win7AppQual/compatibility---application-manifest">compatibility manifest</a> that targets Windows 8. Windows 8 still supports 8-bit and 16-bit color modes for desktop apps that were built without a Windows 8 manifest; Windows 8 emulates these modes but still runs in 32-bit color mode.</div><div> </div>

## -parameters

### -param lpszDeviceName [in]

A pointer to a null-terminated string that specifies the display device whose graphics mode will change. Only display device names as returned by <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a> are valid. See <b>EnumDisplayDevices</b> for further information on the names associated with these display devices.

The <i>lpszDeviceName</i> parameter can be <b>NULL</b>. A <b>NULL</b> value specifies the default display device. The default device can be determined by calling <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a> and checking for the DISPLAY_DEVICE_PRIMARY_DEVICE flag.

### -param lpDevMode [in]

A pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure that describes the new graphics mode. If <i>lpDevMode</i> is <b>NULL</b>, all the values currently in the registry will be used for the display setting. Passing <b>NULL</b> for the <i>lpDevMode</i> parameter and 0 for the <i>dwFlags</i> parameter is the easiest way to return to the default mode after a dynamic mode change.

The <b>dmSize</b> member must be initialized to the size, in bytes, of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. The <b>dmDriverExtra</b> member must be initialized to indicate the number of bytes of private driver data following the <b>DEVMODE</b> structure. In addition, you can use any of the following members of the <b>DEVMODE</b> structure.

<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>dmBitsPerPel</b></td>
<td>Bits per pixel</td>
</tr>
<tr>
<td><b>dmPelsWidth</b></td>
<td>Pixel width</td>
</tr>
<tr>
<td><b>dmPelsHeight</b></td>
<td>Pixel height</td>
</tr>
<tr>
<td><b>dmDisplayFlags</b></td>
<td>Mode flags</td>
</tr>
<tr>
<td><b>dmDisplayFrequency</b></td>
<td>Mode frequency</td>
</tr>
<tr>
<td><b>dmPosition</b></td>
<td>Position of the device in a multi-monitor configuration.</td>
</tr>
</table>
 

In addition to using one or more of the preceding <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> members, you must also set one or more of the following values in the <b>dmFields</b> member to change the display settings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DM_BITSPERPEL</td>
<td>Use the <b>dmBitsPerPel</b> value.</td>
</tr>
<tr>
<td>DM_PELSWIDTH</td>
<td>Use the <b>dmPelsWidth</b> value.</td>
</tr>
<tr>
<td>DM_PELSHEIGHT</td>
<td>Use the <b>dmPelsHeight</b> value.</td>
</tr>
<tr>
<td>DM_DISPLAYFLAGS</td>
<td>Use the <b>dmDisplayFlags</b> value.</td>
</tr>
<tr>
<td>DM_DISPLAYFREQUENCY</td>
<td>Use the <b>dmDisplayFrequency</b> value.</td>
</tr>
<tr>
<td>DM_POSITION</td>
<td>Use the <b>dmPosition</b> value.</td>
</tr>
</table>

### -param hwnd

Reserved; must be <b>NULL</b>.

### -param dwflags [in]

Indicates how the graphics mode should be changed. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The graphics mode for the current screen will be changed dynamically.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_FULLSCREEN"></a><a id="cds_fullscreen"></a><dl>
<dt><b>CDS_FULLSCREEN</b></dt>
</dl>
</td>
<td width="60%">
The mode is temporary in nature.

 If you change to and from another desktop, this mode will not be reset.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_GLOBAL"></a><a id="cds_global"></a><dl>
<dt><b>CDS_GLOBAL</b></dt>
</dl>
</td>
<td width="60%">
The settings will be saved in the global settings area so that they will affect all users on the machine. Otherwise, only the settings for the user are modified. This flag is only valid when specified with the CDS_UPDATEREGISTRY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_NORESET"></a><a id="cds_noreset"></a><dl>
<dt><b>CDS_NORESET</b></dt>
</dl>
</td>
<td width="60%">
The settings will be saved in the registry, but will not take effect. This flag is only valid when specified with the CDS_UPDATEREGISTRY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_RESET"></a><a id="cds_reset"></a><dl>
<dt><b>CDS_RESET</b></dt>
</dl>
</td>
<td width="60%">
The settings should be changed, even if the requested settings are the same as the current settings.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_SET_PRIMARY"></a><a id="cds_set_primary"></a><dl>
<dt><b>CDS_SET_PRIMARY</b></dt>
</dl>
</td>
<td width="60%">
This device will become the primary device.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_TEST"></a><a id="cds_test"></a><dl>
<dt><b>CDS_TEST</b></dt>
</dl>
</td>
<td width="60%">
The system tests if the requested graphics mode could be set.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_UPDATEREGISTRY"></a><a id="cds_updateregistry"></a><dl>
<dt><b>CDS_UPDATEREGISTRY</b></dt>
</dl>
</td>
<td width="60%">
The graphics mode for the current screen will be changed dynamically and the graphics mode will be updated in the registry. The mode information is stored in the USER profile.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_VIDEOPARAMETERS"></a><a id="cds_videoparameters"></a><dl>
<dt><b>CDS_VIDEOPARAMETERS</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>lParam</i> parameter is a pointer to a <a href="/previous-versions/dd145196(v=vs.85)">VIDEOPARAMETERS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_ENABLE_UNSAFE_MODES"></a><a id="cds_enable_unsafe_modes"></a><dl>
<dt><b>CDS_ENABLE_UNSAFE_MODES</b></dt>
</dl>
</td>
<td width="60%">
Enables settings changes to unsafe graphics modes.

</td>
</tr>
<tr>
<td width="40%"><a id="CDS_DISABLE_UNSAFE_MODES"></a><a id="cds_disable_unsafe_modes"></a><dl>
<dt><b>CDS_DISABLE_UNSAFE_MODES</b></dt>
</dl>
</td>
<td width="60%">
Disables settings changes to unsafe graphics modes.

</td>
</tr>
</table>
 

Specifying CDS_TEST allows an application to determine which graphics modes are actually valid, without causing the system to change to them.

If CDS_UPDATEREGISTRY is specified and it is possible to change the graphics mode dynamically, the information is stored in the registry and DISP_CHANGE_SUCCESSFUL is returned. If it is not possible to change the graphics mode dynamically, the information is stored in the registry and DISP_CHANGE_RESTART is returned.

If CDS_UPDATEREGISTRY is specified and the information could not be stored in the registry, the graphics mode is not changed and DISP_CHANGE_NOTUPDATED is returned.

### -param lParam [in]

If <i>dwFlags</i> is <b>CDS_VIDEOPARAMETERS</b>, <i>lParam</i> is a pointer to a <a href="/previous-versions/dd145196(v=vs.85)">VIDEOPARAMETERS</a> structure. Otherwise <i>lParam</i> must be <b>NULL</b>.

## -returns

The <b>ChangeDisplaySettingsEx</b> function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_SUCCESSFUL</b></dt>
</dl>
</td>
<td width="60%">
The settings change was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_BADDUALVIEW</b></dt>
</dl>
</td>
<td width="60%">
The settings change was unsuccessful because the system is DualView capable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_BADFLAGS</b></dt>
</dl>
</td>
<td width="60%">
An invalid set of flags was passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_BADMODE</b></dt>
</dl>
</td>
<td width="60%">
The graphics mode is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_BADPARAM</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed in. This can include an invalid flag or combination of flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The display driver failed the specified graphics mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_NOTUPDATED</b></dt>
</dl>
</td>
<td width="60%">
Unable to write settings to the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_CHANGE_RESTART</b></dt>
</dl>
</td>
<td width="60%">
The computer must be restarted for the graphics mode to work.

</td>
</tr>
</table>

## -remarks

To ensure that the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure passed to <b>ChangeDisplaySettingsEx</b> is valid and contains only values supported by the display driver, use the <b>DEVMODE</b> returned by the <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a> function.

When adding a display monitor to a multiple-monitor system programmatically, set <b>DEVMODE.dmFields</b> to DM_POSITION and specify a position (in <b>DEVMODE.dmPosition</b>) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor. To detach the monitor, set <b>DEVMODE.dmFields</b> to DM_POSITION but set <b>DEVMODE.dmPelsWidth</b> and <b>DEVMODE.dmPelsHeight</b> to zero. For more information, see <a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors</a>.

When the display mode is changed dynamically, the <a href="/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a> message is sent to all running applications with the following message parameters.

<table>
<tr>
<th>Parameters</th>
<th>Meaning</th>
</tr>
<tr>
<td>wParam</td>
<td>New bits per pixel</td>
</tr>
<tr>
<td>LOWORD(lParam)</td>
<td>New pixel width</td>
</tr>
<tr>
<td>HIWORD(lParam)</td>
<td>New pixel height</td>
</tr>
</table>
 

To change the settings for more than one display at the same time, first call <b>ChangeDisplaySettingsEx</b> for each device individually to update the registry without applying the changes. Then call <b>ChangeDisplaySettingsEx</b> once more, with a <b>NULL</b> device, to apply the changes. For example, to change the settings for two displays, do the following:


```cpp

ChangeDisplaySettingsEx (lpszDeviceName1, lpDevMode1, NULL, (CDS_UPDATEREGISTRY | CDS_NORESET), NULL);
ChangeDisplaySettingsEx (lpszDeviceName2, lpDevMode2, NULL, (CDS_UPDATEREGISTRY | CDS_NORESET), NULL);
ChangeDisplaySettingsEx (NULL, NULL, NULL, 0, NULL);

```


<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The input given is always in terms of physical pixels, and is not related to the calling context.





> [!NOTE]
> The winuser.h header defines ChangeDisplaySettingsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesa">EnumDisplayDevices</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a>



<a href="/previous-versions/dd145196(v=vs.85)">VIDEOPARAMETERS</a>



<a href="/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a>
