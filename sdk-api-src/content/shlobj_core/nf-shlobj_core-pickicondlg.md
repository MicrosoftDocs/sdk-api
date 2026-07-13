---
UID: NF:shlobj_core.PickIconDlg
title: PickIconDlg function (shlobj_core.h)
description: PickIconDlg may be altered or unavailable.
helpviewer_keywords: ["PickIconDlg","PickIconDlg function [Windows Shell]","_win32_PickIconDlg","shell.PickIconDlg","shlobj_core/PickIconDlg"]
old-location: shell\PickIconDlg.htm
tech.root: shell
ms.assetid: 3dfcda10-26d8-495d-8c92-7ff16da098c1
ms.date: 12/05/2018
ms.keywords: PickIconDlg, PickIconDlg function [Windows Shell], _win32_PickIconDlg, shell.PickIconDlg, shlobj_core/PickIconDlg
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PickIconDlg
 - shlobj_core/PickIconDlg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - PickIconDlg
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# PickIconDlg function


## -description

<p class="CCE_Message">[<b>PickIconDlg</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays a dialog box that allows the user to choose an icon from the selection available embedded in a resource such as an executable or DLL file.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window. This value can be <b>NULL</b>.

### -param pszIconPath [in, out]

Type: <b>PWSTR</b>

A pointer to a string that contains the null-terminated, fully qualified path of the default resource that contains the icons. If the user chooses a different resource in the dialog, this buffer contains the path of that file when the function returns. This buffer should be at least MAX_PATH characters in length, or the returned path may be truncated. You should verify that the path is valid before using it.

### -param cchIconPath

Type: <b>UINT</b>

The number of characters in <i>pszIconPath</i>, including the terminating <b>NULL</b> character.

### -param piIconIndex [in, out, optional]

Type: <b>int*</b>

A pointer to an integer that on entry specifies the index of the initial selection and, when this function returns successfully, receives the index of the icon that was selected.

## -returns

Type: <b>int</b>

Returns 1 if successful; otherwise, 0.

