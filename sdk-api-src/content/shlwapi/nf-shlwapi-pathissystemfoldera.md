---
UID: NF:shlwapi.PathIsSystemFolderA
title: PathIsSystemFolderA function (shlwapi.h)
description: Determines if an existing folder contains the attributes that make it a system folder. Alternately, this function indicates if certain attributes qualify a folder to be a system folder. (ANSI)
helpviewer_keywords: ["PathIsSystemFolderA", "shlwapi/PathIsSystemFolderA"]
old-location: shell\PathIsSystemFolder.htm
tech.root: shell
ms.assetid: 796901a8-1bc1-4fd1-b5b8-acd8f930ff14
ms.date: 12/05/2018
ms.keywords: PathIsSystemFolder, PathIsSystemFolder function [Windows Shell], PathIsSystemFolderA, PathIsSystemFolderW, _win32_PathIsSystemFolder, shell.PathIsSystemFolder, shlwapi/PathIsSystemFolder, shlwapi/PathIsSystemFolderA, shlwapi/PathIsSystemFolderW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsSystemFolderW (Unicode) and PathIsSystemFolderA (ANSI)
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
 - PathIsSystemFolderA
 - shlwapi/PathIsSystemFolderA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - PathIsSystemFolder
 - PathIsSystemFolderA
 - PathIsSystemFolderW
---

# PathIsSystemFolderA function


## -description

Determines if an existing folder contains the attributes that make it a system folder. Alternately, this function indicates if certain attributes qualify a folder to be a system folder.

## -parameters

### -param pszPath [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the name of an existing folder. The attributes for this folder will be retrieved and compared with those that define a system folder. If this folder contains the attributes to make it a system folder, the function returns nonzero. If this value is <b>NULL</b>, this function determines if the attributes passed in <i>dwAttrb</i> qualify it to be a system folder.

### -param dwAttrb [in]

Type: <b>DWORD</b>

The file attributes to be compared. Used only if <i>pszPath</i> is <b>NULL</b>. In that case, the attributes passed in this value are compared with those that qualify a folder as a system folder. If the attributes are sufficient to make this a system folder, this function returns nonzero. These attributes are the attributes that are returned from <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>.

## -returns

Type: <b>BOOL</b>

Returns nonzero if the <i>pszPath</i> or <i>dwAttrb</i> represent a system folder, or zero otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathIsSystemFolder as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
