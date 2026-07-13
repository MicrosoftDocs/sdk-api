---
UID: NS:winuser.tagRAWINPUTDEVICE
title: RAWINPUTDEVICE (winuser.h)
description: Defines information for the raw input devices.
helpviewer_keywords: ["*LPRAWINPUTDEVICE","*PRAWINPUTDEVICE","LPRAWINPUTDEVICE","LPRAWINPUTDEVICE structure pointer [Keyboard and Mouse Input]","PRAWINPUTDEVICE","PRAWINPUTDEVICE structure pointer [Keyboard and Mouse Input]","RAWINPUTDEVICE","RAWINPUTDEVICE structure [Keyboard and Mouse Input]","RIDEV_APPKEYS","RIDEV_CAPTUREMOUSE","RIDEV_DEVNOTIFY","RIDEV_EXCLUDE","RIDEV_EXINPUTSINK","RIDEV_INPUTSINK","RIDEV_NOHOTKEYS","RIDEV_NOLEGACY","RIDEV_PAGEONLY","RIDEV_REMOVE","_win32_RAWINPUTDEVICE_str","_win32_rawinputdevice_str_cpp","inputdev.rawinputdevice","winui._win32_rawinputdevice_str","winuser/LPRAWINPUTDEVICE","winuser/PRAWINPUTDEVICE","winuser/RAWINPUTDEVICE"]
old-location: inputdev\rawinputdevice.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinputdevice.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWINPUTDEVICE, *PRAWINPUTDEVICE, LPRAWINPUTDEVICE, LPRAWINPUTDEVICE structure pointer [Keyboard and Mouse Input], PRAWINPUTDEVICE, PRAWINPUTDEVICE structure pointer [Keyboard and Mouse Input], RAWINPUTDEVICE, RAWINPUTDEVICE structure [Keyboard and Mouse Input], RIDEV_APPKEYS, RIDEV_CAPTUREMOUSE, RIDEV_DEVNOTIFY, RIDEV_EXCLUDE, RIDEV_EXINPUTSINK, RIDEV_INPUTSINK, RIDEV_NOHOTKEYS, RIDEV_NOLEGACY, RIDEV_PAGEONLY, RIDEV_REMOVE, _win32_RAWINPUTDEVICE_str, _win32_rawinputdevice_str_cpp, inputdev.rawinputdevice, winui._win32_rawinputdevice_str, winuser/LPRAWINPUTDEVICE, winuser/PRAWINPUTDEVICE, winuser/RAWINPUTDEVICE'
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
req.typenames: RAWINPUTDEVICE, *PRAWINPUTDEVICE, *LPRAWINPUTDEVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRAWINPUTDEVICE
 - winuser/tagRAWINPUTDEVICE
 - PRAWINPUTDEVICE
 - winuser/PRAWINPUTDEVICE
 - RAWINPUTDEVICE
 - winuser/RAWINPUTDEVICE
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
 - RAWINPUTDEVICE
---

# RAWINPUTDEVICE structure


## -description

Defines information for the raw input devices.

## -struct-fields

### -field usUsagePage

Type: <b>USHORT</b>

[Top level collection](/windows-hardware/drivers/hid/top-level-collections) [Usage page](/windows-hardware/drivers/hid/hid-usages#usage-page) for the raw input device. See [HID Clients Supported in Windows](/windows-hardware/drivers/hid/hid-architecture#hid-clients-supported-in-windows) for details on possible values.

### -field usUsage

Type: <b>USHORT</b>

[Top level collection](/windows-hardware/drivers/hid/top-level-collections) [Usage ID](/windows-hardware/drivers/hid/hid-usages#usage-id) for the raw input device. See [HID Clients Supported in Windows](/windows-hardware/drivers/hid/hid-architecture#hid-clients-supported-in-windows) for details on possible values.

### -field dwFlags

Type: <b>DWORD</b>

Mode flag that specifies how to interpret the information provided by <b>usUsagePage</b> and <b>usUsage</b>. It can be zero (the default) or one of the following values. By default, the operating system sends raw input from devices with the specified [top level collection](/windows-hardware/drivers/hid/top-level-collections) (TLC) to the registered application as long as it has the window focus. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RIDEV_REMOVE"></a><a id="ridev_remove"></a><dl>
<dt><b>RIDEV_REMOVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If set, this removes the top level collection from the inclusion list. This tells the operating system to stop reading from a device which matches the top level collection.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_EXCLUDE"></a><a id="ridev_exclude"></a><dl>
<dt><b>RIDEV_EXCLUDE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If set, this specifies the top level collections to exclude when reading a complete usage page. This flag only affects a TLC whose usage page is already specified with <b>RIDEV_PAGEONLY</b>. 
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_PAGEONLY"></a><a id="ridev_pageonly"></a><dl>
<dt><b>RIDEV_PAGEONLY</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
If set, this specifies all devices whose top level collection is from the specified <b>usUsagePage</b>. Note that <b>usUsage</b> must be zero. To exclude a particular top level collection, use <b>RIDEV_EXCLUDE</b>.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_NOLEGACY"></a><a id="ridev_nolegacy"></a><dl>
<dt><b>RIDEV_NOLEGACY</b></dt>
<dt>0x00000030</dt>
</dl>
</td>
<td width="60%">
If set, this prevents any devices specified by <b>usUsagePage</b> or <b>usUsage</b> from generating <a href="/windows/win32/inputdev/mouse-input-notifications">legacy messages</a>. This is only for the mouse and keyboard. See Remarks.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_INPUTSINK"></a><a id="ridev_inputsink"></a><dl>
<dt><b>RIDEV_INPUTSINK</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
If set, this enables the caller to receive the input even when the caller is not in the foreground.  Note that <b>hwndTarget</b> must be specified.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_CAPTUREMOUSE"></a><a id="ridev_capturemouse"></a><dl>
<dt><b>RIDEV_CAPTUREMOUSE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
If set, the mouse button click does not activate the other window. <b>RIDEV_CAPTUREMOUSE</b> can be specified only if <b>RIDEV_NOLEGACY</b> is specified for a mouse device.  
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_NOHOTKEYS"></a><a id="ridev_nohotkeys"></a><dl>
<dt><b>RIDEV_NOHOTKEYS</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
If set, the application-defined keyboard device hotkeys are not handled. However, the system hotkeys; for example, ALT+TAB and CTRL+ALT+DEL, are still handled. By default, all keyboard hotkeys are handled. <b>RIDEV_NOHOTKEYS</b> can be specified even if <b>RIDEV_NOLEGACY</b> is not specified and <b>hwndTarget</b> is <b>NULL</b>.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_APPKEYS"></a><a id="ridev_appkeys"></a><dl>
<dt><b>RIDEV_APPKEYS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If set, the application command keys are handled. <b>RIDEV_APPKEYS</b> can be specified only if <b>RIDEV_NOLEGACY</b> is specified for a keyboard device.
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_EXINPUTSINK"></a><a id="ridev_exinputsink"></a><dl>
<dt><b>RIDEV_EXINPUTSINK</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
If set, this enables the caller to receive input in the background only if the foreground application does not process it. In other words, if the foreground application is not registered for raw input, then the background application that is registered will receive the input.
<br><b>Windows XP:</b> This flag is not supported until Windows Vista
</td>
</tr>
<tr>
<td width="40%"><a id="RIDEV_DEVNOTIFY"></a><a id="ridev_devnotify"></a><dl>
<dt><b>RIDEV_DEVNOTIFY</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
If set, this enables the caller to receive <a href="/windows/desktop/inputdev/wm-input-device-change">WM_INPUT_DEVICE_CHANGE</a> notifications for device arrival and device removal.
<br><b>Windows XP:</b> This flag is not supported until Windows Vista
</td>
</tr>
</table>

### -field hwndTarget

Type: <b>HWND</b>

A handle to the target window. If <b>NULL</b>, raw input events follow the keyboard focus to ensure only the focused application window receives the events.

## -remarks

If <b>RIDEV_NOLEGACY</b> is set for a mouse or a keyboard, the system does not generate any legacy message for that device for the application. For example, if the mouse TLC is set with <b>RIDEV_NOLEGACY</b>, **WM_LBUTTONDOWN** and <a href="/windows/win32/inputdev/mouse-input-notifications">related legacy mouse messages</a> are not generated. Likewise, if the keyboard TLC is set with <b>RIDEV_NOLEGACY</b>, **WM_KEYDOWN** and <a href="/windows/win32/inputdev/keyboard-input-notifications">related legacy keyboard messages</a> are not generated.

If <b>RIDEV_REMOVE</b> is set and the <b>hwndTarget</b> member is not set to <b>NULL</b>, then [RegisterRawInputDevices](nf-winuser-registerrawinputdevices.md) function will fail.

## -see-also

<b>Conceptual</b>

[GetRegisteredRawInputDevices](nf-winuser-getregisteredrawinputdevices.md)

[Raw Input](/windows/desktop/inputdev/raw-input)

[Introduction to Human Interface Devices (HID)](/windows-hardware/drivers/hid/)

[HID Clients Supported in Windows](/windows-hardware/drivers/hid/hid-architecture#hid-clients-supported-in-windows)

[HID USB homepage](https://www.usb.org/hid)

<b>Reference</b>

[RegisterRawInputDevices](nf-winuser-registerrawinputdevices.md)
