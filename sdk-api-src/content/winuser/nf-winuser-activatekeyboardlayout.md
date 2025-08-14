---
UID: NF:winuser.ActivateKeyboardLayout
title: ActivateKeyboardLayout function (winuser.h)
description: Sets the input locale identifier (formerly called the keyboard layout handle) for the calling thread or the current process. The input locale identifier specifies a locale as well as the physical layout of the keyboard.
helpviewer_keywords: ["ActivateKeyboardLayout","ActivateKeyboardLayout function [Keyboard and Mouse Input]","HKL_NEXT","HKL_PREV","KLF_REORDER","KLF_RESET","KLF_SETFORPROCESS","KLF_SHIFTLOCK","KLF_UNLOADPREVIOUS","_win32_ActivateKeyboardLayout","_win32_activatekeyboardlayout_cpp","inputdev.activatekeyboardlayout","winui._win32_activatekeyboardlayout","winuser/ActivateKeyboardLayout"]
old-location: inputdev\activatekeyboardlayout.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\activatekeyboardlayout.htm
ms.date: 12/05/2018
ms.keywords: ActivateKeyboardLayout, ActivateKeyboardLayout function [Keyboard and Mouse Input], HKL_NEXT, HKL_PREV, KLF_REORDER, KLF_RESET, KLF_SETFORPROCESS, KLF_SHIFTLOCK, KLF_UNLOADPREVIOUS, _win32_ActivateKeyboardLayout, _win32_activatekeyboardlayout_cpp, inputdev.activatekeyboardlayout, winui._win32_activatekeyboardlayout, winuser/ActivateKeyboardLayout
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ActivateKeyboardLayout
 - winuser/ActivateKeyboardLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - ActivateKeyboardLayout
---

# ActivateKeyboardLayout function


## -description

Sets the input locale identifier (formerly called the keyboard layout handle) for the calling thread or the current process. The input locale identifier specifies a locale as well as the physical layout of the keyboard.

## -parameters

### -param hkl [in]

Type: <b>HKL</b>

Input locale identifier to be activated.

The input locale identifier must have been loaded by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a> function. This parameter must be either the handle to a keyboard layout or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HKL_NEXT"></a><a id="hkl_next"></a><dl>
<dt><b>HKL_NEXT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Selects the next locale identifier in the circular list of loaded locale identifiers maintained by the system.

</td>
</tr>
<tr>
<td width="40%"><a id="HKL_PREV"></a><a id="hkl_prev"></a><dl>
<dt><b>HKL_PREV</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Selects the previous locale identifier in the circular list of loaded locale identifiers maintained by the system.

</td>
</tr>
</table>

### -param Flags [in]

Type: <b>UINT</b>

Specifies how the input locale identifier is to be activated. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KLF_REORDER"></a><a id="klf_reorder"></a><dl>
<dt><b>KLF_REORDER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
If this bit is set, the system's circular list of loaded locale identifiers is reordered by moving the locale identifier to the head of the list. If this bit is not set, the list is rotated without a change of order.

For example, if a user had an English locale identifier active, as well as having French, German, and Spanish locale identifiers loaded (in that order), then activating the German locale identifier with the <b>KLF_REORDER</b> bit set would produce the following order: German, English, French, Spanish. Activating the German locale identifier without the <b>KLF_REORDER</b> bit set would produce the following order: German, Spanish, English, French.

If less than three locale identifiers are loaded, the value of this flag is irrelevant.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_RESET"></a><a id="klf_reset"></a><dl>
<dt><b>KLF_RESET</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
If set but <b>KLF_SHIFTLOCK</b> is not set, the Caps Lock state is turned off by pressing the Caps Lock key again. If set and <b>KLF_SHIFTLOCK</b> is also set, the Caps Lock state is turned off by pressing either SHIFT key.

These two methods are mutually exclusive, and the setting persists as part of the User's profile in the registry.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_SETFORPROCESS"></a><a id="klf_setforprocess"></a><dl>
<dt><b>KLF_SETFORPROCESS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Activates the specified locale identifier for the entire process and sends the 
      <a href="/windows/desktop/winmsg/wm-inputlangchange">WM_INPUTLANGCHANGE</a> message to the current thread's focus or active window.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_SHIFTLOCK"></a><a id="klf_shiftlock"></a><dl>
<dt><b>KLF_SHIFTLOCK</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
This is used with <b>KLF_RESET</b>. See <b>KLF_RESET</b> for an explanation.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_UNLOADPREVIOUS"></a><a id="klf_unloadprevious"></a><dl>
<dt><b>KLF_UNLOADPREVIOUS</b></dt>
</dl>
</td>
<td width="60%">
This flag is unsupported. Use the <a href="/windows/desktop/api/winuser/nf-winuser-unloadkeyboardlayout">UnloadKeyboardLayout</a> function instead.

</td>
</tr>
</table>

## -returns

Type: <b>HKL</b>

The return value is of type 
      <b>HKL</b>. If the function succeeds, the return value is the previous input locale identifier. Otherwise, it is zero.

To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

This function only affects the layout for the current process or thread.

This function is not restricted to keyboard layouts. The 
    <i>hkl</i> parameter is actually an input locale identifier. This is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input. Several input locale identifiers can be loaded at any one time, but only one is active at a time. Loading multiple input locale identifiers makes it possible to rapidly switch between them.

When multiple IMEs are allowed for each locale, passing an input locale identifier in which the high word (the device handle) is zero activates the first IME in the list belonging to the locale.

The <b>KLF_RESET</b> and <b>KLF_SHIFTLOCK</b> flags alter the method by which the Caps Lock state is turned off. By default, the Caps Lock state is turned off by hitting the Caps Lock key again. If only <b>KLF_RESET</b> is set, the default state is reestablished. If <b>KLF_RESET</b> and <b>KLF_SHIFTLOCK</b> are set, the Caps Lock state is turned off by pressing either Caps Lock key. This feature is used to conform to local keyboard behavior standards as well as for personal preferences.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardlayoutnamea">GetKeyboardLayoutName</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-unloadkeyboardlayout">UnloadKeyboardLayout</a>