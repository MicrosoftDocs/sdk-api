---
UID: NS:winuser.tagRID_DEVICE_INFO
title: RID_DEVICE_INFO (winuser.h)
description: Defines the raw input data coming from any device.
helpviewer_keywords: ["*LPRID_DEVICE_INFO","*PRID_DEVICE_INFO","LPRID_DEVICE_INFO","LPRID_DEVICE_INFO structure pointer [Keyboard and Mouse Input]","PRID_DEVICE_INFO","PRID_DEVICE_INFO structure pointer [Keyboard and Mouse Input]","RID_DEVICE_INFO","RID_DEVICE_INFO structure [Keyboard and Mouse Input]","RIM_TYPEHID","RIM_TYPEKEYBOARD","RIM_TYPEMOUSE","_win32_RID_DEVICE_INFO_str","_win32_rid_device_info_str_cpp","inputdev.rid_device_info","winui._win32_rid_device_info_str","winuser/LPRID_DEVICE_INFO","winuser/PRID_DEVICE_INFO","winuser/RID_DEVICE_INFO"]
old-location: inputdev\rid_device_info.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rid_device_info.htm
ms.date: 12/05/2018
ms.keywords: '*LPRID_DEVICE_INFO, *PRID_DEVICE_INFO, LPRID_DEVICE_INFO, LPRID_DEVICE_INFO structure pointer [Keyboard and Mouse Input], PRID_DEVICE_INFO, PRID_DEVICE_INFO structure pointer [Keyboard and Mouse Input], RID_DEVICE_INFO, RID_DEVICE_INFO structure [Keyboard and Mouse Input], RIM_TYPEHID, RIM_TYPEKEYBOARD, RIM_TYPEMOUSE, _win32_RID_DEVICE_INFO_str, _win32_rid_device_info_str_cpp, inputdev.rid_device_info, winui._win32_rid_device_info_str, winuser/LPRID_DEVICE_INFO, winuser/PRID_DEVICE_INFO, winuser/RID_DEVICE_INFO'
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
targetos: Windows
req.typenames: RID_DEVICE_INFO, *PRID_DEVICE_INFO, *LPRID_DEVICE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRID_DEVICE_INFO
 - winuser/tagRID_DEVICE_INFO
 - PRID_DEVICE_INFO
 - winuser/PRID_DEVICE_INFO
 - RID_DEVICE_INFO
 - winuser/RID_DEVICE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RID_DEVICE_INFO
---

# RID_DEVICE_INFO structure


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
<td width="40%"><a id="RIM_TYPEMOUSE"></a><a id="rim_typemouse"></a><dl>
<dt><b>RIM_TYPEMOUSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Data comes from a mouse.
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
<td width="40%"><a id="RIM_TYPEHID"></a><a id="rim_typehid"></a><dl>
<dt><b>RIM_TYPEHID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Data comes from an HID that is not a keyboard or a mouse.
</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.mouse

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_mouse">RID_DEVICE_INFO_MOUSE</a></b>

If <b>dwType</b> is <b>RIM_TYPEMOUSE</b>, this is the <a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_mouse">RID_DEVICE_INFO_MOUSE</a> structure that defines the mouse.

### -field DUMMYUNIONNAME.keyboard

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_keyboard">RID_DEVICE_INFO_KEYBOARD</a></b>

If <b>dwType</b> is <b>RIM_TYPEKEYBOARD</b>, this is the <a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_keyboard">RID_DEVICE_INFO_KEYBOARD</a> structure that defines the keyboard.

### -field DUMMYUNIONNAME.hid

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_hid">RID_DEVICE_INFO_HID</a></b>

If <b>dwType</b> is <b>RIM_TYPEHID</b>, this is the <a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_hid">RID_DEVICE_INFO_HID</a> structure that defines the HID device.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-getrawinputdeviceinfoa">GetRawInputDeviceInfo</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_hid">RID_DEVICE_INFO_HID</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_keyboard">RID_DEVICE_INFO_KEYBOARD</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rid_device_info_mouse">RID_DEVICE_INFO_MOUSE</a>

<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>

<b>Reference</b>