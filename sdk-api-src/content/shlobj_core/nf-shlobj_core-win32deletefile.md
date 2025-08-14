---
UID: NF:shlobj_core.Win32DeleteFile
title: Win32DeleteFile function (shlobj_core.h)
description: Win32DeleteFile may be altered or unavailable.
helpviewer_keywords: ["Win32DeleteFile","Win32DeleteFile function [Windows Shell]","_shell_Win32DeleteFile","shell.Win32DeleteFile","shlobj_core/Win32DeleteFile"]
old-location: shell\Win32DeleteFile.htm
tech.root: shell
ms.assetid: e6b2ac77-a206-413e-aba7-0fd627799a95
ms.date: 12/05/2018
ms.keywords: Win32DeleteFile, Win32DeleteFile function [Windows Shell], _shell_Win32DeleteFile, shell.Win32DeleteFile, shlobj_core/Win32DeleteFile
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Win32DeleteFile
 - shlobj_core/Win32DeleteFile
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
 - Win32DeleteFile
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# Win32DeleteFile function


## -description

<p class="CCE_Message">[<b>Win32DeleteFile</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes a file.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the full name of the file to delete.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the file was successfully deleted; otherwise <b>FALSE</b>.

