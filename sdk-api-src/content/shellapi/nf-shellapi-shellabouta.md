---
UID: NF:shellapi.ShellAboutA
title: ShellAboutA function (shellapi.h)
description: Displays a ShellAbout dialog box. (ANSI)
helpviewer_keywords: ["ShellAboutA", "shellapi/ShellAboutA"]
old-location: shell\ShellAbout.htm
tech.root: shell
ms.assetid: 0919e356-84e8-475e-8628-23097b19c50d
ms.date: 12/05/2018
ms.keywords: ShellAbout, ShellAbout function [Windows Shell], ShellAboutA, ShellAboutW, _win32_ShellAbout, shell.ShellAbout, shellapi/ShellAbout, shellapi/ShellAboutA, shellapi/ShellAboutW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ShellAboutW (Unicode) and ShellAboutA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 3.51 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShellAboutA
 - shellapi/ShellAboutA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - ShellAbout
 - ShellAboutA
 - ShellAboutW
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# ShellAboutA function


## -description

Displays a <b>ShellAbout</b> dialog box.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A window handle to a parent window. This parameter can be <b>NULL</b>.

### -param szApp [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains text to be displayed in the title bar of the <b>ShellAbout</b> dialog box and on the first line of the dialog box after the text "Microsoft". If the text contains a separator (#) that divides it into two parts, the function displays the first part in the title bar and the second part on the first line after the text "Microsoft".

                    

<b>Windows 2000, Windows XP, Windows Server 2003</b>: If the string pointed to by this parameter contains a separator (#), then the string must be writable.

<b>Windows Vista, Windows Server 2008</b>: This string cannot exceed 200 characters in length. The contents of <b>szApp</b> will no longer show after "Microsoft", unless there is a # separator, in which case the part after the # will completely replace the first line.

### -param szOtherStuff [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains text to be displayed in the dialog box after the version and copyright information. This parameter can be <b>NULL</b>.

### -param hIcon [in, optional]

Type: <b>HICON</b>

The handle of an icon that the function displays in the dialog box. This parameter can be <b>NULL</b>, in which case the function displays the Windows icon.

## -returns

Type: <b>int</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

Note that the <b>ShellAbout</b> function dialog box uses text and a default icon that are specific to Windows.

To see an example of a <b>ShellAbout</b> dialog box, run the `winver.exe` command.




> [!NOTE]
> The shellapi.h header defines ShellAbout as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

