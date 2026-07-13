---
UID: NF:winuser.GetRawInputDeviceInfoW
title: GetRawInputDeviceInfoW function (winuser.h)
description: Retrieves information about the raw input device. (Unicode)
helpviewer_keywords: ["GetRawInputDeviceInfo", "GetRawInputDeviceInfo function [Keyboard and Mouse Input]", "GetRawInputDeviceInfoW", "RIDI_DEVICEINFO", "RIDI_DEVICENAME", "RIDI_PREPARSEDDATA", "_win32_GetRawInputDeviceInfo", "_win32_getrawinputdeviceinfo_cpp", "inputdev.getrawinputdeviceinfo", "winui._win32_getrawinputdeviceinfo", "winuser/GetRawInputDeviceInfo", "winuser/GetRawInputDeviceInfoW"]
old-location: inputdev\getrawinputdeviceinfo.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputdeviceinfo.htm
ms.date: 12/05/2018
ms.keywords: GetRawInputDeviceInfo, GetRawInputDeviceInfo function [Keyboard and Mouse Input], GetRawInputDeviceInfoA, GetRawInputDeviceInfoW, RIDI_DEVICEINFO, RIDI_DEVICENAME, RIDI_PREPARSEDDATA, _win32_GetRawInputDeviceInfo, _win32_getrawinputdeviceinfo_cpp, inputdev.getrawinputdeviceinfo, winui._win32_getrawinputdeviceinfo, winuser/GetRawInputDeviceInfo, winuser/GetRawInputDeviceInfoA, winuser/GetRawInputDeviceInfoW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetRawInputDeviceInfoW (Unicode) and GetRawInputDeviceInfoA (ANSI)
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
 - GetRawInputDeviceInfoW
 - winuser/GetRawInputDeviceInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-rawinput-l1-2-0.dll
 - ext-ms-win-rtcore-ntuser-rawinput-l1-1-1.dll
 - ext-ms-win-ntuser-rawinput-l1-2-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetRawInputDeviceInfo
 - GetRawInputDeviceInfoA
 - GetRawInputDeviceInfoW
req.apiset: ext-ms-win-ntuser-rawinput-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetRawInputDeviceInfoW function


## -description

Retrieves information about the raw input device.

## -parameters

### -param hDevice [in, optional]

Type: <b>HANDLE</b>

A handle to the raw input device. This comes from the <b>hDevice</b> member of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a> or from <a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist">GetRawInputDeviceList</a>.

### -param uiCommand [in]

Type: <b>UINT</b>

Specifies what data will be returned in <i>pData</i>. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RIDI_PREPARSEDDATA"></a><a id="ridi_preparseddata"></a><dl>
<dt><b>RIDI_PREPARSEDDATA</b></dt>
<dt>0x20000005</dt>
</dl>
</td>
<td width="60%">
<i>pData</i> is a <a href="/windows-hardware/drivers/ddi/hidclass/ni-hidclass-ioctl_hid_get_collection_descriptor">PHIDP_PREPARSED_DATA</a> pointer to a buffer for a <a href="/windows-hardware/drivers/hid/top-level-collections">top-level collection's</a> <a href="/windows-hardware/drivers/hid/preparsed-data">preparsed data</a>.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDI_DEVICENAME"></a><a id="ridi_devicename"></a><dl>
<dt><b>RIDI_DEVICENAME</b></dt>
<dt>0x20000007</dt>
</dl>
</td>
<td width="60%">
<i>pData</i> points to a string that contains the <a href="/windows-hardware/drivers/wdf/using-device-interfaces">device interface name</a>.

If this device is <a href="/windows-hardware/drivers/hid/hid-architecture#hid-clients-supported-in-windows">opened with Shared Access Mode</a> then you can call <a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> with this name to open a HID collection and use returned handle for calling <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a> to read input reports and <a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a> to send output reports.

For more information, see <a href="/windows-hardware/drivers/hid/opening-hid-collections">Opening HID Collections</a> and <a href="/windows-hardware/drivers/hid/handling-hid-reports">Handling HID Reports</a>.

For this <i>uiCommand</i> only, the value in <i>pcbSize</i> is the character count (not the byte count).
</td>
</tr>
<tr>
<td width="40%"><a id="RIDI_DEVICEINFO"></a><a id="ridi_deviceinfo"></a><dl>
<dt><b>RIDI_DEVICEINFO</b></dt>
<dt>0x2000000b</dt>
</dl>
</td>
<td width="60%">
<i>pData</i> points to an <a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info">RID_DEVICE_INFO</a> structure.
</td>
</tr>
</table>

### -param pData [in, out, optional]

Type: <b>LPVOID</b>

A pointer to a buffer that contains the information specified by <i>uiCommand</i>. Pointer should be aligned on a **DWORD** (32-bit) boundary.

If <i>uiCommand</i> is <b>RIDI_DEVICEINFO</b>, set the <b>cbSize</b> member of <a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info">RID_DEVICE_INFO</a> to <code>sizeof(RID_DEVICE_INFO)</code> before calling <b>GetRawInputDeviceInfo</b>.

### -param pcbSize [in, out]

Type: <b>PUINT</b>

The size, in bytes, of the data in <i>pData</i>.

## -returns

Type: <b>UINT</b>

If successful, this function returns a non-negative number indicating the number of bytes copied to <i>pData</i>. 

If <i>pData</i> is not large enough for the data, the function returns -1. If <i>pData</i> is <b>NULL</b>, the function returns a value of zero. In both of these cases, <i>pcbSize</i> is set to the minimum size required for the <i>pData</i> buffer.

Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to identify any other errors.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info">RID_DEVICE_INFO</a>

<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>

<b>Reference</b>

<a href="/windows/desktop/inputdev/wm-input">WM_INPUT</a>

<a href="/windows-hardware/drivers/hid/top-level-collections">Top-Level Collections</a>

<a href="/windows-hardware/drivers/hid/preparsed-data">Preparsed Data</a>

<a href="/windows-hardware/drivers/ddi/hidclass/ni-hidclass-ioctl_hid_get_collection_descriptor">PHIDP_PREPARSED_DATA</a>

<a href="/windows-hardware/drivers/hid/opening-hid-collections">Opening HID collections</a>

<a href="/windows-hardware/drivers/hid/handling-hid-reports">Handling HID Reports</a>

## -remarks

> [!NOTE]
> The winuser.h header defines GetRawInputDeviceInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
