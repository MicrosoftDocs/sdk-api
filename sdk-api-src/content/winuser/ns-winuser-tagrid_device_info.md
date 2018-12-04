---
UID: NS:winuser.tagRID_DEVICE_INFO
title: tagRID_DEVICE_INFO
author: windows-sdk-content
description: Defines the raw input data coming from any device.
old-location: inputdev\rid_device_info.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rid_device_info.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPRID_DEVICE_INFO, *PRID_DEVICE_INFO, LPRID_DEVICE_INFO, LPRID_DEVICE_INFO structure pointer [Keyboard and Mouse Input], PRID_DEVICE_INFO, PRID_DEVICE_INFO structure pointer [Keyboard and Mouse Input], RID_DEVICE_INFO, RID_DEVICE_INFO structure [Keyboard and Mouse Input], RIM_TYPEHID, RIM_TYPEKEYBOARD, RIM_TYPEMOUSE, _win32_RID_DEVICE_INFO_str, _win32_rid_device_info_str_cpp, inputdev.rid_device_info, tagRID_DEVICE_INFO, winui._win32_rid_device_info_str, winuser/LPRID_DEVICE_INFO, winuser/PRID_DEVICE_INFO, winuser/RID_DEVICE_INFO"
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
 - RID_DEVICE_INFO
product: Windows
targetos: Windows
req.typenames: RID_DEVICE_INFO, *PRID_DEVICE_INFO, *LPRID_DEVICE_INFO
req.redist: 
---

# tagRID_DEVICE_INFO structure


## -description


Defines the raw input data coming from any device. 


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of the <b>RID_DEVICE_INFO</b> structure. 


### -field dwType

Type: <b>DWORD</b>

The type of raw input data. This member can be one of the following values. 

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
Data comes from an HID that is not a keyboard or a mouse.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEKEYBOARD"></a><a id="rim_typekeyboard"></a><dl>
<dt><b>RIM_TYPEKEYBOARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Data comes from a keyboard.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEMOUSE"></a><a id="rim_typemouse"></a><dl>
<dt><b>RIM_TYPEMOUSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Data comes from a mouse.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.mouse

Type: <b><a href="https://msdn.microsoft.com/ada5510d-0e3a-4663-a98a-80ea0517f28d">RID_DEVICE_INFO_MOUSE</a></b>

If <b>dwType</b> is <b>RIM_TYPEMOUSE</b>, this is the <a href="https://msdn.microsoft.com/ada5510d-0e3a-4663-a98a-80ea0517f28d">RID_DEVICE_INFO_MOUSE</a> structure that defines the mouse. 


### -field DUMMYUNIONNAME.keyboard

Type: <b><a href="https://msdn.microsoft.com/1f93ea56-66d0-46db-9da9-af0042ffb5b9">RID_DEVICE_INFO_KEYBOARD</a></b>

If <b>dwType</b> is <b>RIM_TYPEKEYBOARD</b>, this is the <a href="https://msdn.microsoft.com/1f93ea56-66d0-46db-9da9-af0042ffb5b9">RID_DEVICE_INFO_KEYBOARD</a> structure that defines the keyboard. 


### -field DUMMYUNIONNAME.hid

Type: <b><a href="https://msdn.microsoft.com/77769507-7e23-4c4d-954e-cd1770b49426">RID_DEVICE_INFO_HID</a></b>

If <b>dwType</b> is <b>RIM_TYPEHID</b>, this is the <a href="https://msdn.microsoft.com/77769507-7e23-4c4d-954e-cd1770b49426">RID_DEVICE_INFO_HID</a> structure that defines the HID device. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1d8316d3-83ed-4f8b-bed4-09533d6f3591">GetRawInputDeviceInfo</a>



<a href="https://msdn.microsoft.com/77769507-7e23-4c4d-954e-cd1770b49426">RID_DEVICE_INFO_HID</a>



<a href="https://msdn.microsoft.com/1f93ea56-66d0-46db-9da9-af0042ffb5b9">RID_DEVICE_INFO_KEYBOARD</a>



<a href="https://msdn.microsoft.com/ada5510d-0e3a-4663-a98a-80ea0517f28d">RID_DEVICE_INFO_MOUSE</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

