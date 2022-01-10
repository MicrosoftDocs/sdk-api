---
UID: NF:winuser.GetRawInputDeviceList
title: GetRawInputDeviceList function (winuser.h)
description: Enumerates the raw input devices attached to the system.
helpviewer_keywords: ["GetRawInputDeviceList","GetRawInputDeviceList function [Keyboard and Mouse Input]","_win32_GetRawInputDeviceList","_win32_getrawinputdevicelist_cpp","inputdev.getrawinputdevicelist","winui._win32_getrawinputdevicelist","winuser/GetRawInputDeviceList"]
old-location: inputdev\getrawinputdevicelist.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputdevicelist.htm
ms.date: 12/05/2018
ms.keywords: GetRawInputDeviceList, GetRawInputDeviceList function [Keyboard and Mouse Input], _win32_GetRawInputDeviceList, _win32_getrawinputdevicelist_cpp, inputdev.getrawinputdevicelist, winui._win32_getrawinputdevicelist, winuser/GetRawInputDeviceList
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetRawInputDeviceList
 - winuser/GetRawInputDeviceList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-SysParaMS-Ext-L1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetRawInputDeviceList
req.apiset: ext-ms-win-ntuser-rawinput-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetRawInputDeviceList function


## -description

Enumerates the raw input devices attached to the system.

## -parameters

### -param pRawInputDeviceList [out, optional]

Type: <b>PRAWINPUTDEVICELIST</b>

An array of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevicelist">RAWINPUTDEVICELIST</a> structures for the devices attached to the system. If <b>NULL</b>, the number of devices are returned in *<i>puiNumDevices</i>.

### -param puiNumDevices [in, out]

Type: <b>PUINT</b>

If <i>pRawInputDeviceList</i> is <b>NULL</b>, the function populates this variable with the number of devices attached to the system; otherwise, this variable specifies the number of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevicelist">RAWINPUTDEVICELIST</a> structures that can be contained in the buffer to which <i>pRawInputDeviceList</i> points. If this value is less than the number of devices attached to the system, the function returns the actual number of devices in this variable and fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.

### -param cbSize [in]

Type: <b>UINT</b>

The size of a <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevicelist">RAWINPUTDEVICELIST</a> structure, in bytes.

## -returns

Type: <b>UINT</b>

If the function is successful, the return value is the number of devices stored in the buffer pointed to by 
						<i>pRawInputDeviceList</i>.

On any other error, the function returns (<b>UINT</b>) -1 and 
						<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the error indication.

## -remarks

The devices returned from this function are the mouse, the keyboard, and other Human Interface Device (HID) devices.

To get more detailed information about the attached devices, call <a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdeviceinfoa">GetRawInputDeviceInfo</a> using the hDevice from <a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevicelist">RAWINPUTDEVICELIST</a>. 


#### Examples

The following sample code shows a typical call to <b>GetRawInputDeviceList</b>:


```cpp
UINT nDevices, nStored, i;
PRAWINPUTDEVICELIST pRawInputDeviceList;
if (GetRawInputDeviceList(NULL, &nDevices, sizeof(RAWINPUTDEVICELIST)) != 0) { Error(); }

// The list of devices can change between calls to GetRawInputDeviceList,
// so call it again if the function returns ERROR_INSUFFICIENT_BUFFER
do
{
    if ((pRawInputDeviceList = realloc(sizeof(RAWINPUTDEVICELIST) * nDevices)) == NULL) { Error(); }
    nStored = GetRawInputDeviceList(pRawInputDeviceList, &nDevices, sizeof(RAWINPUTDEVICELIST));
} while (nStored == (UINT)-1 && GetLastError() == ERROR_INSUFFICIENT_BUFFER);

if (nStored == (UINT)-1) { Error(); }

for (i = 0; i < nStored; ++i)
{
    // do the job with each pRawInputDeviceList[i] element...
}

// after the job, free the RAWINPUTDEVICELIST
free(pRawInputDeviceList);
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdeviceinfoa">GetRawInputDeviceInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-rawinputdevicelist">RAWINPUTDEVICELIST</a>



<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
