---
UID: NF:shlwapi.PathSetDlgItemPathW
title: PathSetDlgItemPathW function (shlwapi.h)
description: Sets the text of a child control in a window or dialog box, using PathCompactPath to ensure the path fits in the control. (Unicode)
helpviewer_keywords: ["PathSetDlgItemPath", "PathSetDlgItemPath function [Windows Shell]", "PathSetDlgItemPathW", "_win32_PathSetDlgItemPath", "shell.PathSetDlgItemPath", "shlwapi/PathSetDlgItemPath", "shlwapi/PathSetDlgItemPathW"]
old-location: shell\PathSetDlgItemPath.htm
tech.root: shell
ms.assetid: 05737525-d906-482c-847f-bdbf0ba0ce3d
ms.date: 12/05/2018
ms.keywords: PathSetDlgItemPath, PathSetDlgItemPath function [Windows Shell], PathSetDlgItemPathA, PathSetDlgItemPathW, _win32_PathSetDlgItemPath, shell.PathSetDlgItemPath, shlwapi/PathSetDlgItemPath, shlwapi/PathSetDlgItemPathA, shlwapi/PathSetDlgItemPathW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathSetDlgItemPathW (Unicode) and PathSetDlgItemPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathSetDlgItemPathW
 - shlwapi/PathSetDlgItemPathW
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
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathSetDlgItemPath
 - PathSetDlgItemPathA
 - PathSetDlgItemPathW
---

# PathSetDlgItemPathW function


## -description

Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcompactpatha">PathCompactPath</a> to ensure the path fits in the control.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box or window.

### -param id [in]

Type: <b>int</b>

The identifier of the control.

### -param pszPath [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to set in the control.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathSetDlgItemPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
