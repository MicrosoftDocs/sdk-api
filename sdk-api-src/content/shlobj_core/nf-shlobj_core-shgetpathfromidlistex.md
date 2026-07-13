---
UID: NF:shlobj_core.SHGetPathFromIDListEx
title: SHGetPathFromIDListEx function (shlobj_core.h)
description: Converts an item identifier list to a file system path. This function extends SHGetPathFromIDList by allowing you to set the initial size of the string buffer and declare the options below.
helpviewer_keywords: ["GPFIDL_ALTNAME","GPFIDL_DEFAULT","GPFIDL_UNCPRINTER","SHGetPathFromIDListEx","SHGetPathFromIDListEx function [Windows Shell]","_shell_SHGetPathFromIDListEx","shell.SHGetPathFromIDListEx","shlobj_core/SHGetPathFromIDListEx"]
old-location: shell\SHGetPathFromIDListEx.htm
tech.root: shell
ms.assetid: 80270c59-275d-4b13-b16c-0c07bb79ed8e
ms.date: 12/05/2018
ms.keywords: GPFIDL_ALTNAME, GPFIDL_DEFAULT, GPFIDL_UNCPRINTER, SHGetPathFromIDListEx, SHGetPathFromIDListEx function [Windows Shell], _shell_SHGetPathFromIDListEx, shell.SHGetPathFromIDListEx, shlobj_core/SHGetPathFromIDListEx
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetPathFromIDListEx
 - shlobj_core/SHGetPathFromIDListEx
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
api_name:
 - SHGetPathFromIDListEx
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHGetPathFromIDListEx function


## -description

Converts an item identifier list to a file system path. This function extends <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista">SHGetPathFromIDList</a> by allowing you to set the initial size of the string buffer and declare the options below.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an item identifier list that specifies a file or directory location relative to the root of the namespace (the desktop).

### -param pszPath [out]

Type: <b>PWSTR</b>

When this function is called it is passed a null-terminated, Unicode buffer to receive the file system path. This buffer is of size <i>cchPath</i>. 
                        
                        

When this function returns, contains the address of a null-terminated, Unicode buffer that contains the file system path. This buffer is of size <i>cchPath</i>.

### -param cchPath

Type: <b>DWORD</b>

The size of the buffer pointed to by <i>pszPath</i>, in characters.

### -param uOpts

Type: <b>GPFIDL_FLAGS</b>

These flags determine the type of path returned.



#### GPFIDL_DEFAULT (0x0000)

Win32 file names, servers, and root drives are included.



#### GPFIDL_ALTNAME (0x0001)

Uses short file names.



#### GPFIDL_UNCPRINTER (0x0002)

Include UNC printer names items.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

Except for UNC printer names, if the location specified by the <i>pidl</i> parameter is not part of the file system, this function fails.

If the <i>pidl</i> parameter specifies a shortcut, the <i>pszPath</i> contains the path to the shortcut, not to the shortcut's target.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname">SHParseDisplayName</a>
