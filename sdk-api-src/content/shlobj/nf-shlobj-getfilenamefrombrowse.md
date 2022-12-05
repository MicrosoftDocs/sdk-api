---
UID: NF:shlobj.GetFileNameFromBrowse
title: GetFileNameFromBrowse function (shlobj.h)
description: The GetFileNameFromBrowse function creates an Open dialog box so that the user can specify the drive, directory, and name of a file to open.
helpviewer_keywords: ["GetFileNameFromBrowse","GetFileNameFromBrowse function [Windows Shell]","_win32_GetFileNameFromBrowse","shell.GetFileNameFromBrowse","shlobj_core/GetFileNameFromBrowse"]
old-location: shell\GetFileNameFromBrowse.htm
tech.root: shell
ms.assetid: 1f075051-18c8-4ec2-b010-f983ba2d3303
ms.date: 08/02/2022
ms.keywords: GetFileNameFromBrowse, GetFileNameFromBrowse function [Windows Shell], _win32_GetFileNameFromBrowse, shell.GetFileNameFromBrowse, shlobj_core/GetFileNameFromBrowse
req.header: shlobj.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetFileNameFromBrowse
 - shlobj/GetFileNameFromBrowse
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
 - GetFileNameFromBrowse
---

# GetFileNameFromBrowse function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates an <b>Open</b> dialog box so that the user can specify the drive, directory, and name of a file to open.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner.

### -param pszFilePath [in, out]

Type: <b>PWSTR</b>

A null-terminated Unicode string that contains a file name used to initialize the File Name edit control. This string corresponds to the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure's <b>lpstrFile</b> member and is used in exactly the same way.

### -param cchFilePath

Type: <b>UINT</b>

The number of characters in <i>pszFilePath</i>, including the terminating null character.

### -param pszWorkingDir [in, optional]

Type: <b>PCWSTR</b>

The fully qualified file path of the initial directory. This string corresponds to the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure's <b>lpstrInitialDir</b> member and is used in exactly the same way.

### -param pszDefExt [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the default file name extension. This extension is added to <i>pszFilePath</i> if the user does not specify an extension. The string should not contain any '.' characters. If this string is <b>NULL</b> and the user fails to type an extension, no extension is appended.

### -param pszFilters [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that defines the filter. This string corresponds to the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure's <b>lpstrFilter</b> member and is used in exactly the same way.

### -param pszTitle [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that is placed in the title bar of the dialog box. If this value is <b>NULL</b>, the system uses the default title.

## -returns

Type: <b>BOOL</b>

If the user specifies a file name and clicks <b>OK</b>, the return value is <b>TRUE</b>. The buffer that <i>pszFilePath</i> points to contains the full path and file name that the user specifies. If the user cancels or closes the <b>Open</b> dialog box or an error occurs, the return value is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a>
