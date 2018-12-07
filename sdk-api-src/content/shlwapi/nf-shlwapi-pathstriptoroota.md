---
UID: NF:shlwapi.PathStripToRootA
title: PathStripToRootA function
author: windows-sdk-content
description: Removes all file and directory elements in a path except for the root information.
old-location: shell\PathStripToRoot.htm
tech.root: shell
ms.assetid: ce9a1a40-2a03-44d2-80bc-0dc10654550b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PathStripToRoot, PathStripToRoot function [Windows Shell], PathStripToRootA, PathStripToRootW, _win32_PathStripToRoot, shell.PathStripToRoot, shlwapi/PathStripToRoot, shlwapi/PathStripToRootA, shlwapi/PathStripToRootW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathStripToRootW (Unicode) and PathStripToRootA (ANSI)
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
 - PathStripToRoot
 - PathStripToRootA
 - PathStripToRootW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathStripToRootA function


## -description


Removes all file and directory elements in a path except for the root information.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/e0539478-8c64-4445-ab99-22f1df70afe8">PathCchStripToRoot</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be converted. When this function returns successfully, this string contains only the root information taken from that path.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if a valid drive letter was found in the path, or <b>FALSE</b> otherwise.



