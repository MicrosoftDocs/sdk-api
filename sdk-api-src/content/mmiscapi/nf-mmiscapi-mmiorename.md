---
UID: NF:mmiscapi.mmioRename
title: mmioRename function (mmiscapi.h)
description: The mmioRename function renames the specified file and contains parameters that modify strings containing a file name.
helpviewer_keywords: ["_win32_mmioRename","mmioRename","mmioRename function [Windows Multimedia]","mmioRenameA","mmioRenameW","mmsystem/mmioRename","mmsystem/mmioRenameA","mmsystem/mmioRenameW","multimedia.mmiorename"]
old-location: multimedia\mmiorename.htm
tech.root: Multimedia
ms.assetid: f47ef581-b3c8-409b-9edf-cbc8cfa04036
ms.date: 08/02/2022
ms.keywords: _win32_mmioRename, mmioRename, mmioRename function [Windows Multimedia], mmioRenameA, mmioRenameW, mmsystem/mmioRename, mmsystem/mmioRenameA, mmsystem/mmioRenameW, multimedia.mmiorename
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mmioRenameW (Unicode) and mmioRenameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmioRename
 - mmiscapi/mmioRename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioRename
 - mmioRenameA
 - mmioRenameW
---

# mmioRename function


## -description

The <b>mmioRename</b> function renames the specified file.

## -parameters

### -param pszFileName

Pointer to a string containing the file name of the file to rename.

### -param pszNewFileName

Pointer to a string containing the new file name.

### -param pmmioinfo

Pointer to an <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure containing extra parameters used by <b>mmioRename</b>. If this parameter is not <b>NULL</b>, all unused members of the <b>MMIOINFO</b> structure it references must be set to zero, including the reserved members.

### -param fdwRename

Flags for the rename operation. This parameter should be set to zero.

## -returns

Returns zero if the file was renamed. Otherwise, returns an error code returned from <b>mmioRename</b> or from the I/O procedure.
