---
UID: NF:shlwapi.PathIsHTMLFileA
title: PathIsHTMLFileA macro (shlwapi.h)
description: Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension. (ANSI)
helpviewer_keywords: ["PathIsHTMLFileA", "shlwapi/PathIsHTMLFileA"]
old-location: shell\PathIsHTMLFile.htm
tech.root: shell
ms.assetid: f24f82c8-ce32-4fbd-be49-06817cc57e5b
ms.date: 12/05/2018
ms.keywords: PathIsHTMLFile, PathIsHTMLFile function [Windows Shell], PathIsHTMLFileA, PathIsHTMLFileW, _win32_PathIsHTMLFile, shell.PathIsHTMLFile, shlwapi/PathIsHTMLFile, shlwapi/PathIsHTMLFileA, shlwapi/PathIsHTMLFileW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsHTMLFileW (Unicode) and PathIsHTMLFileA (ANSI)
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
 - PathIsHTMLFileA
 - shlwapi/PathIsHTMLFileA
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
 - PathIsHTMLFile
 - PathIsHTMLFileA
 - PathIsHTMLFileW
---

# PathIsHTMLFileA macro


## -description

Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

The address of a character buffer that contains the path and name of the file.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathIsHTMLFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

