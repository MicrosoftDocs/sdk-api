---
UID: NF:winuser.GetRawInputDeviceInfoA
title: GetRawInputDeviceInfoA function
author: windows-sdk-content
description: Retrieves information about the raw input device.
old-location: inputdev\getrawinputdeviceinfo.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputdeviceinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetRawInputDeviceInfo, GetRawInputDeviceInfo function [Keyboard and Mouse Input], GetRawInputDeviceInfoA, GetRawInputDeviceInfoW, RIDI_DEVICEINFO, RIDI_DEVICENAME, RIDI_PREPARSEDDATA, _win32_GetRawInputDeviceInfo, _win32_getrawinputdeviceinfo_cpp, inputdev.getrawinputdeviceinfo, winui._win32_getrawinputdeviceinfo, winuser/GetRawInputDeviceInfo, winuser/GetRawInputDeviceInfoA, winuser/GetRawInputDeviceInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetRawInputDeviceInfoW (Unicode) and GetRawInputDeviceInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetRawInputDeviceInfo
 - GetRawInputDeviceInfoA
 - GetRawInputDeviceInfoW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetRawInputDeviceInfoA function


## -description


Retrieves information about the raw input device.


## -parameters




### -param hDevice [in, optional]

Type: <b>HANDLE</b>

A handle to the raw input device. This comes from the <b>hDevice</b> member of <a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a> or from <a href="https://msdn.microsoft.com/0283e578-8f6c-4239-b856-99d8812f588b">GetRawInputDeviceList</a>. 


### -param uiCommand [in]

Type: <b>UINT</b>

Specifies what data will be returned in 
					<i>pData</i>. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RIDI_DEVICENAME"></a><a id="ridi_devicename"></a><dl>
<dt><b>RIDI_DEVICENAME</b></dt>
<dt>0x20000007</dt>
</dl>
</td>
<td width="60%">
<i>pData</i> points to a string that contains the device name. 

For this 
						<i>uiCommand</i> only, the value in 
						<i>pcbSize</i> is the character count (not the byte count).

</td>
</tr>
<tr>
<td width="40%"><a id="RIDI_DEVICEINFO"></a><a id="ridi_deviceinfo"></a><dl>
<dt><b>RIDI_DEVICEINFO</b></dt>
<dt>0x2000000b</dt>
</dl>
</td>
<td width="60%">
<i>pData</i> points to an <a href="https://msdn.microsoft.com/1d44f5b1-2dbb-4a49-b8c0-8f65bb3fa79a">RID_DEVICE_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RIDI_PREPARSEDDATA"></a><a id="ridi_preparseddata"></a><dl>
<dt><b>RIDI_PREPARSEDDATA</b></dt>
<dt>0x20000005</dt>
</dl>
</td>
<td width="60%">
<i>pData</i> points to the previously parsed data.

</td>
</tr>
</table>
 


### -param pData [in, out, optional]

Type: <b>LPVOID</b>

A pointer to a buffer that contains the information specified by 
					<i>uiCommand</i>. If 
					<i>uiCommand</i> is <b>RIDI_DEVICEINFO</b>, set the <b>cbSize</b> member of <a href="https://msdn.microsoft.com/1d44f5b1-2dbb-4a49-b8c0-8f65bb3fa79a">RID_DEVICE_INFO</a> to <code>sizeof(RID_DEVICE_INFO)</code> before calling <b>GetRawInputDeviceInfo</b>. 


### -param pcbSize [in, out]

Type: <b>PUINT</b>

The size, in bytes, of the data in 
					<i>pData</i>. 


## -returns



Type: <b>UINT</b>

If successful, this function returns a non-negative number indicating the number of bytes copied to 
						<i>pData</i>. 

If 
						<i>pData</i> is not large enough for the data, the function returns -1. If 
						<i>pData</i> is <b>NULL</b>, the function returns a value of zero. In both of these cases, 
						<i>pcbSize</i> is set to the minimum size required for the 
						<i>pData</i> buffer.

Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to identify any other errors.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a>



<a href="https://msdn.microsoft.com/1d44f5b1-2dbb-4a49-b8c0-8f65bb3fa79a">RID_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a>
 

 

