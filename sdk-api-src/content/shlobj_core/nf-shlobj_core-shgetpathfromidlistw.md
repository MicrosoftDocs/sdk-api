---
UID: NF:shlobj_core.SHGetPathFromIDListW
title: SHGetPathFromIDListW function (shlobj_core.h)
description: Converts an item identifier list to a file system path. (Unicode)
helpviewer_keywords: ["SHGetPathFromIDList", "SHGetPathFromIDList function [Windows Shell]", "SHGetPathFromIDListW", "_win32_SHGetPathFromIDList", "shell.SHGetPathFromIDList", "shlobj_core/SHGetPathFromIDList", "shlobj_core/SHGetPathFromIDListW"]
old-location: shell\SHGetPathFromIDList.htm
tech.root: shell
ms.assetid: f043ffa2-37c1-465d-aed6-0475e721fbde
ms.date: 12/05/2018
ms.keywords: SHGetPathFromIDList, SHGetPathFromIDList function [Windows Shell], SHGetPathFromIDListA, SHGetPathFromIDListW, _win32_SHGetPathFromIDList, shell.SHGetPathFromIDList, shlobj_core/SHGetPathFromIDList, shlobj_core/SHGetPathFromIDListA, shlobj_core/SHGetPathFromIDListW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetPathFromIDListW (Unicode) and SHGetPathFromIDListA (ANSI)
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
 - SHGetPathFromIDListW
 - shlobj_core/SHGetPathFromIDListW
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
 - windows.storage.dll
api_name:
 - SHGetPathFromIDList
 - SHGetPathFromIDListA
 - SHGetPathFromIDListW
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHGetPathFromIDListW function


## -description

Converts an item identifier list to a file system path.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The address of an item identifier list that specifies a file or directory location relative to the root of the namespace (the desktop).

### -param pszPath [out]

Type: <b>LPTSTR</b>

The address of a buffer to receive the file system path. This buffer must be at least MAX_PATH characters in size.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

If the location specified by the <i>pidl</i> parameter is not part of the file system, this function will fail.

If the <i>pidl</i> parameter specifies a shortcut, the <i>pszPath</i> will contain the path to the shortcut, not to the shortcut's target.





> [!NOTE]
> The shlobj_core.h header defines SHGetPathFromIDList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex">SHGetPathFromIDListEx</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname">SHParseDisplayName</a>
