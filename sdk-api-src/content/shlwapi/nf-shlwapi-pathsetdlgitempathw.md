---
UID: NF:shlwapi.PathSetDlgItemPathW
title: PathSetDlgItemPathW function (shlwapi.h)
description: Sets the text of a child control in a window or dialog box, using PathCompactPath to ensure the path fits in the control.
old-location: shell\PathSetDlgItemPath.htm
tech.root: shell
ms.assetid: 05737525-d906-482c-847f-bdbf0ba0ce3d
ms.date: 12/05/2018
ms.keywords: PathSetDlgItemPath, PathSetDlgItemPath function [Windows Shell], PathSetDlgItemPathA, PathSetDlgItemPathW, _win32_PathSetDlgItemPath, shell.PathSetDlgItemPath, shlwapi/PathSetDlgItemPath, shlwapi/PathSetDlgItemPathA, shlwapi/PathSetDlgItemPathW
f1_keywords:
- shlwapi/PathSetDlgItemPath
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shlwapi.dll
- API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- PathSetDlgItemPath
- PathSetDlgItemPathA
- PathSetDlgItemPathW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathSetDlgItemPathW function


## -description


Sets the text of a child control in a window or dialog box, using <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-pathcompactpatha">PathCompactPath</a> to ensure the path fits in the control.


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


