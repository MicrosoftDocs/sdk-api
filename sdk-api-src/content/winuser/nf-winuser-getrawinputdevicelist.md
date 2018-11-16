---
UID: NF:winuser.GetRawInputDeviceList
title: GetRawInputDeviceList function
author: windows-sdk-content
description: Enumerates the raw input devices attached to the system.
old-location: inputdev\getrawinputdevicelist.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputdevicelist.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRawInputDeviceList, GetRawInputDeviceList function [Keyboard and Mouse Input], _win32_GetRawInputDeviceList, _win32_getrawinputdevicelist_cpp, inputdev.getrawinputdevicelist, winui._win32_getrawinputdevicelist, winuser/GetRawInputDeviceList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetRawInputDeviceList
: 
---

# GetRawInputDeviceList function


## -description


Enumerates the raw input devices attached to the system. 


## -parameters




### -param pRawInputDeviceList [out, optional]

Type: <b>PRAWINPUTDEVICELIST</b>

An array of <a href="https://msdn.microsoft.com/ad2650d7-34dc-40e2-ab24-85dc705058c7">RAWINPUTDEVICELIST</a> structures for the devices attached to the system. If <b>NULL</b>, the number of devices are returned in *<i>puiNumDevices</i>. 


### -param puiNumDevices [in, out]

Type: <b>PUINT</b>

If <i>pRawInputDeviceList</i> is <b>NULL</b>, the function populates this variable with the number of devices attached to the system; otherwise, this variable specifies the number of <a href="https://msdn.microsoft.com/ad2650d7-34dc-40e2-ab24-85dc705058c7">RAWINPUTDEVICELIST</a> structures that can be contained in the buffer to which <i>pRawInputDeviceList</i> points. If this value is less than the number of devices attached to the system, the function returns the actual number of devices in this variable and fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


### -param cbSize [in]

Type: <b>UINT</b>

The size of a <a href="https://msdn.microsoft.com/ad2650d7-34dc-40e2-ab24-85dc705058c7">RAWINPUTDEVICELIST</a> structure, in bytes.


## -returns



Type: <b>UINT</b>

If the function is successful, the return value is the number of devices stored in the buffer pointed to by 
						<i>pRawInputDeviceList</i>.

On any other error, the function returns (<b>UINT</b>) -1 and 
						<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the error indication.




## -remarks



The devices returned from this function are the mouse, the keyboard, and other Human Interface Device (HID) devices.

To get more detailed information about the attached devices, call <a href="https://msdn.microsoft.com/1d8316d3-83ed-4f8b-bed4-09533d6f3591">GetRawInputDeviceInfo</a> using the hDevice from <a href="https://msdn.microsoft.com/ad2650d7-34dc-40e2-ab24-85dc705058c7">RAWINPUTDEVICELIST</a>. 


#### Examples

The following sample code shows a typical call to <b>GetRawInputDeviceList</b>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>UINT nDevices;
PRAWINPUTDEVICELIST pRawInputDeviceList;
if (GetRawInputDeviceList(NULL, &amp;nDevices, sizeof(RAWINPUTDEVICELIST)) != 0) { Error();}
if ((pRawInputDeviceList = malloc(sizeof(RAWINPUTDEVICELIST) * nDevices)) == NULL) {Error();}
if (GetRawInputDeviceList(pRawInputDeviceList, &amp;nDevices, sizeof(RAWINPUTDEVICELIST)) == (&lt;dtype rid="UINT"/&gt;)-1) {Error();}
// do the job...

// after the job, free the RAWINPUTDEVICELIST
free(pRawInputDeviceList);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1d8316d3-83ed-4f8b-bed4-09533d6f3591">GetRawInputDeviceInfo</a>



<a href="https://msdn.microsoft.com/ad2650d7-34dc-40e2-ab24-85dc705058c7">RAWINPUTDEVICELIST</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

