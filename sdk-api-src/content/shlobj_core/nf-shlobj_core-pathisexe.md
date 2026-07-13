---
UID: NF:shlobj_core.PathIsExe
title: PathIsExe function (shlobj_core.h)
description: PathIsExe may be altered or unavailable.
helpviewer_keywords: ["PathIsExe","PathIsExe function [Windows Shell]","_win32_PathIsExe","shell.PathIsExe","shlobj_core/PathIsExe"]
old-location: shell\PathIsExe.htm
tech.root: shell
ms.assetid: 54e9dae7-f9c4-48b8-9b91-32ed21365fb7
ms.date: 12/05/2018
ms.keywords: PathIsExe, PathIsExe function [Windows Shell], _win32_PathIsExe, shell.PathIsExe, shlobj_core/PathIsExe
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathIsExe
 - shlobj_core/PathIsExe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - PathIsExe
---

# PathIsExe function


## -description

<p class="CCE_Message">[<b>PathIsExe</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a file is an executable by examining the file name extension.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the file path, which includes the name of the file.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the file name extension is .cmd, .bat, .pif, .scf, .exe, .com, or .scr; otherwise, <b>FALSE</b>.

