---
UID: NF:shlwapi.PathRenameExtensionA
title: PathRenameExtensionA function (shlwapi.h)
description: Replaces the extension of a file name with a new extension. If the file name does not contain an extension, the extension will be attached to the end of the string.helpviewer_keywords: ["PathRenameExtension","PathRenameExtension function [Windows Shell]","PathRenameExtensionA","PathRenameExtensionW","_win32_PathRenameExtension","shell.PathRenameExtension","shlwapi/PathRenameExtension","shlwapi/PathRenameExtensionA","shlwapi/PathRenameExtensionW"]
old-location: shell\PathRenameExtension.htm
tech.root: shell
ms.assetid: 3d94f67c-e3ee-4b64-b0b9-8f771423bdc5
ms.date: 12/05/2018
ms.keywords: PathRenameExtension, PathRenameExtension function [Windows Shell], PathRenameExtensionA, PathRenameExtensionW, _win32_PathRenameExtension, shell.PathRenameExtension, shlwapi/PathRenameExtension, shlwapi/PathRenameExtensionA, shlwapi/PathRenameExtensionW
f1_keywords:
- shlwapi/PathRenameExtension
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
req.unicode-ansi: PathRenameExtensionW (Unicode) and PathRenameExtensionA (ANSI)
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
- API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
- PathRenameExtension
- PathRenameExtensionA
- PathRenameExtensionW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathRenameExtensionA function


## -description


Replaces the extension of a file name with a new extension. If the file name does not contain an extension, the extension will be attached to the end of the string.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://docs.microsoft.com/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension">PathCchRenameExtension</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a null-terminated string of length MAX_PATH in which to replace the extension.


### -param pszExt [in]

Type: <b>LPCTSTR</b>

Pointer to a character buffer that contains a '.' character followed by the new extension.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero if the new path and extension would exceed MAX_PATH characters.



