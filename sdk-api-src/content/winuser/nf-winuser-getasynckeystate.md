---
UID: NF:winuser.GetAsyncKeyState
title: GetAsyncKeyState function (winuser.h)
description: Determines whether a key is up or down at the time the function is called, and whether the key was pressed after a previous call to GetAsyncKeyState.
helpviewer_keywords: ["GetAsyncKeyState","GetAsyncKeyState function [Keyboard and Mouse Input]","_win32_GetAsyncKeyState","_win32_getasynckeystate_cpp","inputdev.getasynckeystate","winui._win32_getasynckeystate","winuser/GetAsyncKeyState"]
old-location: inputdev\getasynckeystate.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getasynckeystate.htm
ms.date: 12/05/2018
ms.keywords: GetAsyncKeyState, GetAsyncKeyState function [Keyboard and Mouse Input], _win32_GetAsyncKeyState, _win32_getasynckeystate_cpp, inputdev.getasynckeystate, winui._win32_getasynckeystate, winuser/GetAsyncKeyState
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
ms.custom: snippet-project
f1_keywords:
 - GetAsyncKeyState
 - winuser/GetAsyncKeyState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-keyboard-l1-1-0.dll
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - GetAsyncKeyState
---

# GetAsyncKeyState function


## -description

Determines whether a key is up or down at the time the function is called, and whether the key has been pressed since a previous call to <b>GetAsyncKeyState</b>.

## -parameters

### -param vKey [in]

Type: <b>int</b>

The virtual-key code. For more information, see <a href="/windows/desktop/inputdev/virtual-key-codes">Virtual Key Codes</a>.

You can use left- and right-distinguishing constants to specify certain keys. See the Remarks section for further information.

## -returns

Type: <b>SHORT</b>

The most significant bit of the return value is set if the specified key is currently down.
Since the most significant bit is the sign bit, a negative value indicates that the key is currently down.

For backward compatibility,
the least significant bit is set if the specified key has been pressed since the most
recent previous call in the session to <b>GetAsyncKeyState</b> for that key,
but the value is unreliable. (See Remarks.)

All other bits of the result are reserved and should be ignored.

The return value is zero if the call fails.
Reasons for failure include

<ul>
<li>The current desktop is not the active desktop.</li>
<li>UI Privilege Isolation (UIPI) prevents the calling thread from accessing the foreground thread.</li>
<li>The foreground thread belongs to another process and the calling thread does not have <b>DESKTOP_HOOKCONTROL</b> or <b>DESKTOP_JOURNALRECORD</b> access to its desktop.</li>
</ul>

## -remarks

The <b>GetAsyncKeyState</b> function works with mouse buttons. However, it checks on the state of the physical mouse buttons, not on the logical mouse buttons that the physical buttons are mapped to. For example, the call <b>GetAsyncKeyState</b>(VK_LBUTTON) always returns the state of the left physical mouse button, regardless of whether it is mapped to the left or right logical mouse button. You can determine the system's current mapping of physical mouse buttons to logical mouse buttons by calling <code>GetSystemMetrics(SM_SWAPBUTTON)</code>,
which returns TRUE if the mouse buttons have been swapped.

Although the least significant bit of the return value indicates whether the key has been pressed since the last query, due to the preemptive multitasking nature of Windows, another application can call <b>GetAsyncKeyState</b> and receive the "recently pressed" bit instead of your application. The behavior of the least significant bit of the return value is retained for compatibility with 16-bit Windows applications (which are non-preemptive) and should not be relied upon because it can report false negatives.

You can use the virtual-key code constants <b>VK_SHIFT</b>, <b>VK_CONTROL</b>, and <b>VK_MENU</b> as values for the 
    <i>vKey</i> parameter. This gives the state of the SHIFT, CTRL, or ALT keys without distinguishing between left and right.

You can use the following virtual-key code constants as values for 
    <i>vKey</i> to distinguish between the left and right instances of those keys.

<table class="clsStd">
<tr>
<th>Code</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>VK_LSHIFT</b></td>
<td>
Left-shift key.

</td>
</tr>
<tr>
<td><b>VK_RSHIFT</b></td>
<td>
Right-shift key.

</td>
</tr>
<tr>
<td><b>VK_LCONTROL</b></td>
<td>
Left-control key.

</td>
</tr>
<tr>
<td><b>VK_RCONTROL</b></td>
<td>
Right-control key.

</td>
</tr>
<tr>
<td><b>VK_LMENU</b></td>
<td>
Left-menu key.

</td>
</tr>
<tr>
<td><b>VK_RMENU</b></td>
<td>
Right-menu key.

</td>
</tr>
</table>
 

These left- and right-distinguishing constants are only available when you call the <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>, <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>, <b>GetAsyncKeyState</b>, <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeya">MapVirtualKey</a> functions.

## Example

```cpp
int APIENTRY WinMain(HINSTANCE hInst, HINSTANCE hInstPrev, PSTR cmdline, int cmdshow)
{
    BOOL considerSafeMode = FALSE;

    // If the user holds the CTRL key while the app is launching,
    // then offer to enter Safe Mode.
    if (GetAsyncKeyState(VK_CONTROL) < 0)
    {
        considerSafeMode = TRUE;
    }

    ...
}
```

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeya">MapVirtualKey</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
