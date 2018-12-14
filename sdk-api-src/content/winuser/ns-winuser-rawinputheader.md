---
UID: NS:winuser.tagRAWINPUTHEADER
title: RAWINPUTHEADER
author: windows-sdk-content
description: Contains the header information that is part of the raw input data.
old-location: inputdev\rawinputheader.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinputheader.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPRAWINPUTHEADER, *PRAWINPUTHEADER, PRAWINPUTHEADER, PRAWINPUTHEADER structure pointer [Keyboard and Mouse Input], RAWINPUTHEADER, RAWINPUTHEADER structure [Keyboard and Mouse Input], RIM_TYPEHID, RIM_TYPEKEYBOARD, RIM_TYPEMOUSE, _win32_RAWINPUTHEADER_str, _win32_rawinputheader_str_cpp, inputdev.rawinputheader, winui._win32_rawinputheader_str, winuser/PRAWINPUTHEADER, winuser/RAWINPUTHEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RAWINPUTHEADER
product: Windows
targetos: Windows
req.typenames: RAWINPUTHEADER, *PRAWINPUTHEADER, *LPRAWINPUTHEADER
req.redist: 
---

# RAWINPUTHEADER structure


## -description


Contains the header information that is part of the raw input data. 


## -struct-fields




### -field dwType

Type: <b>DWORD</b>

The type of raw input. It can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEHID"></a><a id="rim_typehid"></a><dl>
<dt><b>RIM_TYPEHID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Raw input comes from some device that is not a keyboard or a mouse.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEKEYBOARD"></a><a id="rim_typekeyboard"></a><dl>
<dt><b>RIM_TYPEKEYBOARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Raw input comes from the keyboard.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEMOUSE"></a><a id="rim_typemouse"></a><dl>
<dt><b>RIM_TYPEMOUSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Raw input comes from the mouse.

</td>
</tr>
</table>
 


### -field dwSize

Type: <b>DWORD</b>

The size, in bytes, of the entire input packet of data. This includes <a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a> plus possible extra input reports in the <a href="https://msdn.microsoft.com/en-us/library/ms645549(v=VS.85).aspx">RAWHID</a> variable length array. 


### -field hDevice

Type: <b>HANDLE</b>

A handle to the device generating the raw input data. 


### -field wParam

Type: <b>WPARAM</b>

The value passed in the 
					<i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a> message. 


## -remarks



To get more information on the device, use <b>hDevice</b> in a call to <a href="https://msdn.microsoft.com/en-us/library/ms645597(v=VS.85).aspx">GetRawInputDeviceInfo</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645597(v=VS.85).aspx">GetRawInputDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645549(v=VS.85).aspx">RAWHID</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a>
 

 

