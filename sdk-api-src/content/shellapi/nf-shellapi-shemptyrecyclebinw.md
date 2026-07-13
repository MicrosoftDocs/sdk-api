---
UID: NF:shellapi.SHEmptyRecycleBinW
title: SHEmptyRecycleBinW function (shellapi.h)
description: Empties the Recycle Bin on the specified drive. (Unicode)
helpviewer_keywords: ["SHERB_NOCONFIRMATION", "SHERB_NOPROGRESSUI", "SHERB_NOSOUND", "SHEmptyRecycleBin", "SHEmptyRecycleBin function [Windows Shell]", "SHEmptyRecycleBinW", "_win32_SHEmptyRecycleBin", "shell.SHEmptyRecycleBin", "shellapi/SHEmptyRecycleBin", "shellapi/SHEmptyRecycleBinW"]
old-location: shell\SHEmptyRecycleBin.htm
tech.root: shell
ms.assetid: c3995be7-bc8b-4e1f-8ef6-fdf4c0a75720
ms.date: 12/05/2018
ms.keywords: SHERB_NOCONFIRMATION, SHERB_NOPROGRESSUI, SHERB_NOSOUND, SHEmptyRecycleBin, SHEmptyRecycleBin function [Windows Shell], SHEmptyRecycleBinA, SHEmptyRecycleBinW, _win32_SHEmptyRecycleBin, shell.SHEmptyRecycleBin, shellapi/SHEmptyRecycleBin, shellapi/SHEmptyRecycleBinA, shellapi/SHEmptyRecycleBinW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHEmptyRecycleBinW (Unicode) and SHEmptyRecycleBinA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHEmptyRecycleBinW
 - shellapi/SHEmptyRecycleBinW
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
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHEmptyRecycleBin
 - SHEmptyRecycleBinA
 - SHEmptyRecycleBinW
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHEmptyRecycleBinW function


## -description

Empties the Recycle Bin on the specified drive.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window of any dialog boxes that might be displayed during the operation. This parameter can be <b>NULL</b>.

### -param pszRootPath [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string of maximum length MAX_PATH that contains the path of the root drive on which the Recycle Bin is located. This parameter can contain the address of a string formatted with the drive, folder, and subfolder names, for example c:\windows\system\. It can also contain an empty string or <b>NULL</b>. If this value is an empty string or <b>NULL</b>, all Recycle Bins on all drives will be emptied.

### -param dwFlags

Type: <b>DWORD</b>

One or more of the following values.



#### SHERB_NOCONFIRMATION

No dialog box confirming the deletion of the objects will be displayed.



#### SHERB_NOPROGRESSUI

No dialog box indicating the progress will be displayed.



#### SHERB_NOSOUND

No sound will be played when the operation is complete.


##### - dwFlags.SHERB_NOCONFIRMATION

No dialog box confirming the deletion of the objects will be displayed.


##### - dwFlags.SHERB_NOPROGRESSUI

No dialog box indicating the progress will be displayed.


##### - dwFlags.SHERB_NOSOUND

No sound will be played when the operation is complete.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-shqueryrecyclebina">SHQueryRecycleBin</a>

## -remarks

> [!NOTE]
> The shellapi.h header defines SHEmptyRecycleBin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
