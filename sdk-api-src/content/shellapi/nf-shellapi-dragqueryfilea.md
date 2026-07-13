---
UID: NF:shellapi.DragQueryFileA
title: DragQueryFileA function (shellapi.h)
description: Retrieves the names of dropped files that result from a successful drag-and-drop operation. (ANSI)
helpviewer_keywords: ["DragQueryFileA", "shellapi/DragQueryFileA"]
old-location: shell\DragQueryFile.htm
tech.root: shell
ms.assetid: 93fab381-9035-46c4-ba9d-efb2d0801d84
ms.date: 12/05/2018
ms.keywords: DragQueryFile, DragQueryFile function [Windows Shell], DragQueryFileA, DragQueryFileW, _win32_DragQueryFile, shell.DragQueryFile, shellapi/DragQueryFile, shellapi/DragQueryFileA, shellapi/DragQueryFileW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DragQueryFileW (Unicode) and DragQueryFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DragQueryFileA
 - shellapi/DragQueryFileA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - DragQueryFile
 - DragQueryFileA
 - DragQueryFileW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# DragQueryFileA function


## -description

Retrieves the names of dropped files that result from a successful drag-and-drop operation.

## -parameters

### -param hDrop [in]

Type: <b>HDROP</b>

Identifier of the structure that contains the file names of the dropped files.

### -param iFile [in]

Type: <b>UINT</b>

Index of the file to query. If the value of this parameter is 0xFFFFFFFF, <b>DragQueryFile</b> returns a count of the files dropped. If the value of this parameter is between zero and the total number of files dropped, <b>DragQueryFile</b> copies the file name with the corresponding value to the buffer pointed to by the <i>lpszFile</i> parameter.

### -param lpszFile [out]

Type: <b>LPTSTR</b>

The address of a buffer that receives the file name of a dropped file when the function returns. This file name is a null-terminated string. If this parameter is <b>NULL</b>, <b>DragQueryFile</b> returns the required size, in characters, of this buffer.

### -param cch

Type: <b>UINT</b>

The size, in characters, of the <i>lpszFile</i> buffer.

## -returns

Type: <b>UINT</b>

A nonzero value indicates a successful call.

When the function copies a file name to the buffer, the return value is a count of the characters copied, not including the terminating null character.

If the index value is 0xFFFFFFFF, the return value is a count of the dropped files. Note that the index variable itself returns unchanged, and therefore remains 0xFFFFFFFF.

If the index value is between zero and the total number of dropped files, and the <i>lpszFile</i> buffer address is <b>NULL</b>, the return value is the required size, in characters, of the buffer, <i>not including</i> the terminating null character.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-dragquerypoint">DragQueryPoint</a>

## -remarks

> [!NOTE]
> The shellapi.h header defines DragQueryFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
