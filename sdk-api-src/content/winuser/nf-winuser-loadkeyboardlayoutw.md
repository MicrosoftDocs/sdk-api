---
UID: NF:winuser.LoadKeyboardLayoutW
title: LoadKeyboardLayoutW function (winuser.h)
description: Loads a new input locale identifier (formerly called the keyboard layout) into the system. (Unicode)
helpviewer_keywords: ["KLF_ACTIVATE", "KLF_NOTELLSHELL", "KLF_REORDER", "KLF_REPLACELANG", "KLF_SETFORPROCESS", "KLF_SUBSTITUTE_OK", "KLF_UNLOADPREVIOUS", "LoadKeyboardLayout", "LoadKeyboardLayout function [Keyboard and Mouse Input]", "LoadKeyboardLayoutW", "_win32_LoadKeyboardLayout", "_win32_loadkeyboardlayout_cpp", "inputdev.loadkeyboardlayout", "winui._win32_loadkeyboardlayout", "winuser/LoadKeyboardLayout", "winuser/LoadKeyboardLayoutW"]
old-location: inputdev\loadkeyboardlayout.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\loadkeyboardlayout.htm
ms.date: 12/05/2018
ms.keywords: KLF_ACTIVATE, KLF_NOTELLSHELL, KLF_REORDER, KLF_REPLACELANG, KLF_SETFORPROCESS, KLF_SUBSTITUTE_OK, KLF_UNLOADPREVIOUS, LoadKeyboardLayout, LoadKeyboardLayout function [Keyboard and Mouse Input], LoadKeyboardLayoutA, LoadKeyboardLayoutW, _win32_LoadKeyboardLayout, _win32_loadkeyboardlayout_cpp, inputdev.loadkeyboardlayout, winui._win32_loadkeyboardlayout, winuser/LoadKeyboardLayout, winuser/LoadKeyboardLayoutA, winuser/LoadKeyboardLayoutW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadKeyboardLayoutW (Unicode) and LoadKeyboardLayoutA (ANSI)
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
 - LoadKeyboardLayoutW
 - winuser/LoadKeyboardLayoutW
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
 - ext-ms-win-ntuser-keyboard-l1-3-0.dll
 - User32.dll
api_name:
 - LoadKeyboardLayout
 - LoadKeyboardLayoutA
 - LoadKeyboardLayoutW
---

# LoadKeyboardLayoutW function


## -description

Loads a new input locale identifier (formerly called the keyboard layout) into the system.

<b>Prior to Windows 8:</b> Several input locale identifiers can be loaded at a time, but only one per process is active at a time. Loading multiple input locale identifiers makes it possible to rapidly switch between them.

<b>Beginning in  Windows 8:</b> The input locale identifier is loaded for the entire system. This function has no effect if the current process does not own the window with keyboard focus.

## -parameters

### -param pwszKLID [in]

Type: <b>LPCTSTR</b>

The name of the input locale identifier to load. This name is a string composed of the hexadecimal value of the <a href="/windows/desktop/Intl/language-identifiers">Language Identifier</a> (low word) and a device identifier (high word). For example, U.S. English has a language identifier of 0x0409, so the primary U.S. English layout is named "00000409". Variants of U.S. English layout (such as the Dvorak layout) are named "00010409", "00020409", and so on. 

For a list of the input layouts that are supplied with Windows, see [Keyboard Identifiers and Input Method Editors for Windows](/windows-hardware/manufacture/desktop/windows-language-pack-default-values).

### -param Flags [in]

Type: <b>UINT</b>

Specifies how the input locale identifier is to be loaded. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KLF_ACTIVATE"></a><a id="klf_activate"></a><dl>
<dt><b>KLF_ACTIVATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
<b>Prior to Windows 8:</b> If the specified input locale identifier is not already loaded, the function loads and activates the input locale identifier for the current thread.

<b>Beginning in  Windows 8:</b> If the specified input locale identifier is not already loaded, the function loads and activates the input locale identifier for the system.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_NOTELLSHELL"></a><a id="klf_notellshell"></a><dl>
<dt><b>KLF_NOTELLSHELL</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
<b>Prior to Windows 8:</b> Prevents a <a href="/windows/win32/winmsg/shellproc">ShellProc</a> hook procedure from receiving an <b>HSHELL_LANGUAGE</b> hook code when the new input locale identifier is loaded. This value is typically used when an application loads multiple input locale identifiers one after another. Applying this value to all but the last input locale identifier delays the shell's processing until all input locale identifiers have been added.

<b>Beginning in  Windows 8:</b> In this scenario, the last input locale identifier is set for the entire system.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_REORDER"></a><a id="klf_reorder"></a><dl>
<dt><b>KLF_REORDER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<b>Prior to Windows 8:</b> Moves the specified input locale identifier to the head of the input locale identifier list, making that locale identifier the active locale identifier for the current thread. This value reorders the input locale identifier list even if <b>KLF_ACTIVATE</b> is not provided.

<b>Beginning in  Windows 8:</b> Moves the specified input locale identifier to the head of the input locale identifier list, making that locale identifier the active locale identifier for the system. This value reorders the input locale identifier list even if <b>KLF_ACTIVATE</b> is not provided.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_REPLACELANG"></a><a id="klf_replacelang"></a><dl>
<dt><b>KLF_REPLACELANG</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If the new input locale identifier has the same language identifier as a current input locale identifier, the new input locale identifier replaces the current one as the input locale identifier for that language. If this value is not provided and the input locale identifiers have the same language identifiers, the current input locale identifier is not replaced and the function returns <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_SUBSTITUTE_OK"></a><a id="klf_substitute_ok"></a><dl>
<dt><b>KLF_SUBSTITUTE_OK</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Substitutes the specified input locale identifier with another locale preferred by the user. The system starts with this flag set, and it is recommended that your application always use this flag. The substitution occurs only if the registry key <b>HKEY_CURRENT_USER\Keyboard Layout\Substitutes</b> explicitly defines a substitution locale. For example, if the key includes the value name "00000409" with value "00010409", loading the US layout ("00000409") causes the United States-Dvorak layout ("00010409") to be loaded instead. The system uses <b>KLF_SUBSTITUTE_OK</b> when booting, and it is recommended that all applications use this value when loading input locale identifiers to ensure that the user's preference is selected.

</td>
</tr>
<tr>
<td width="40%"><a id="KLF_SETFORPROCESS"></a><a id="klf_setforprocess"></a><dl>
<dt><b>KLF_SETFORPROCESS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
<b>Prior to Windows 8:</b> This flag is valid only with <b>KLF_ACTIVATE</b>. Activates the specified input locale identifier for the entire process and sends the <a href="/windows/desktop/winmsg/wm-inputlangchange">WM_INPUTLANGCHANGE</a> message to the current thread's Focus or Active window. Typically, <b>LoadKeyboardLayout</b> activates an input locale identifier only for the current thread.

<b>Beginning in  Windows 8:</b> This flag is not used. <b>LoadKeyboardLayout</b> always activates an input locale identifier for the entire system if the current process owns the window with keyboard focus.

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

If the function succeeds, the return value is the input locale identifier corresponding to the name specified in <i>pwszKLID</i>. If no matching locale is available, the return value is the default language of the system.

If the function fails, the return value is NULL. This can occur if the layout library is loaded from the application directory.

To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input. 

An application can and will typically load the default input locale identifier or IME for a language and can do so by specifying only a string version of the language identifier. If an application wants to load a specific locale or IME, it should read the registry to determine the specific input locale identifier to pass to <b>LoadKeyboardLayout</b>. In this case, a request to activate the default input locale identifier for a locale will activate the first matching one. A specific IME should be activated using an explicit input locale identifier returned from <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout">GetKeyboardLayout</a> or <b>LoadKeyboardLayout</b>.

<b>Prior to Windows 8:</b> This function only affects the layout for the current process or thread.

<b>Beginning in  Windows 8:</b> This function affects the layout for the entire system.

> [!NOTE]
> The winuser.h header defines LoadKeyboardLayout as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-activatekeyboardlayout">ActivateKeyboardLayout</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardlayoutnamea">GetKeyboardLayoutName</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-unloadkeyboardlayout">UnloadKeyboardLayout</a>
