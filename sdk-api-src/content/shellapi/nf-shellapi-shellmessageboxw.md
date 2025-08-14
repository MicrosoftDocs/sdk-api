---
UID: NF:shellapi.ShellMessageBoxW
title: ShellMessageBoxW function (shellapi.h)
description: ShellMessageBox may be altered or unavailable. (Unicode)
helpviewer_keywords: ["ShellMessageBox", "ShellMessageBox function [Windows Shell]", "ShellMessageBoxW", "_win32_ShellMessageBox", "shell.ShellMessageBox", "shellapi/ShellMessageBox", "shellapi/ShellMessageBoxW"]
old-location: shell\ShellMessageBox.htm
tech.root: shell
ms.assetid: 7cbaeae3-3473-4568-90ab-63efef049af3
ms.date: 12/05/2018
ms.keywords: ShellMessageBox, ShellMessageBox function [Windows Shell], ShellMessageBoxA, ShellMessageBoxW, _win32_ShellMessageBox, shell.ShellMessageBox, shellapi/ShellMessageBox, shellapi/ShellMessageBoxA, shellapi/ShellMessageBoxW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ShellMessageBoxW (Unicode) and ShellMessageBoxA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShellMessageBoxW
 - shellapi/ShellMessageBoxW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - Ext-MS-Win-shell-shlwapi-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - ShellMessageBox
 - ShellMessageBoxA
 - ShellMessageBoxW
---

# ShellMessageBoxW function


## -description

<p class="CCE_Message">[<b>ShellMessageBox</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

<b>ShellMessageBox</b> is a special instance of <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> that provides the option of using the owner window's title as the title of the message box.

## -parameters

### -param hAppInst [in]

Type: <b>HINSTANCE</b>

The handle of the module from which to load a string resource named in <i>pszTitle</i>. If <i>pszTitle</i> does not name a string resource, this parameter is ignored. This value must be valid if <i>pszMsg</i> or <i>pszTitle</i> is a resource ID.

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the owner window of the message box to be created. If this variable is not <b>NULL</b>, the title of the owner window is used as the title of the message box.

### -param lpcText [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains either the message to be displayed or a resource ID specifying where the message is to be retrieved from.

### -param lpcTitle [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the dialog box title or a resource ID specifying where the title is to be retrieved. If both this parameter and <i>hWnd</i> are <b>NULL</b>, no title is displayed. If this parameter points to a loadable resource formed with the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro, it overrides <i>hWnd</i> as the title.

### -param fuStyle [in]

Type: <b>UINT</b>

Specifies the contents and behavior of the dialog box. For possible values, see <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>.

### -param ...

A variable argument list that is combined with <i>pszMsg</i> to form the full text displayed in the message box.

## -returns

Type: <b>int</b>

An integer value indicating a button that was pressed in the message box. For specific values, see <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>.

					

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>

## -remarks

> [!NOTE]
> The shellapi.h header defines ShellMessageBox as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

