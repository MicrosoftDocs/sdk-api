---
UID: NF:shlobj_core.SHGetPathFromIDListW
title: SHGetPathFromIDListW function (shlobj_core.h)
description: Converts an item identifier list to a file system path.helpviewer_keywords: ["SHGetPathFromIDList","SHGetPathFromIDList function [Windows Shell]","SHGetPathFromIDListA","SHGetPathFromIDListW","_win32_SHGetPathFromIDList","shell.SHGetPathFromIDList","shlobj_core/SHGetPathFromIDList","shlobj_core/SHGetPathFromIDListA","shlobj_core/SHGetPathFromIDListW"]
old-location: shell\SHGetPathFromIDList.htm
tech.root: shell
ms.assetid: f043ffa2-37c1-465d-aed6-0475e721fbde
ms.date: 12/05/2018
ms.keywords: SHGetPathFromIDList, SHGetPathFromIDList function [Windows Shell], SHGetPathFromIDListA, SHGetPathFromIDListW, _win32_SHGetPathFromIDList, shell.SHGetPathFromIDList, shlobj_core/SHGetPathFromIDList, shlobj_core/SHGetPathFromIDListA, shlobj_core/SHGetPathFromIDListW
f1_keywords:
- shlobj_core/SHGetPathFromIDList
dev_langs:
- c++
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
- SHGetPathFromIDList
- SHGetPathFromIDListA
- SHGetPathFromIDListW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex">SHGetPathFromIDListEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname">SHParseDisplayName</a>
 

 

