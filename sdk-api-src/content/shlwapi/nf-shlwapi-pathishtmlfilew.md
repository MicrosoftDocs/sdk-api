---
UID: NF:shlwapi.PathIsHTMLFileW
title: PathIsHTMLFileW macro (shlwapi.h)
description: Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension.
old-location: shell\PathIsHTMLFile.htm
tech.root: shell
ms.assetid: f24f82c8-ce32-4fbd-be49-06817cc57e5b
ms.date: 12/05/2018
ms.keywords: PathIsHTMLFile, PathIsHTMLFile function [Windows Shell], PathIsHTMLFileA, PathIsHTMLFileW, _win32_PathIsHTMLFile, shell.PathIsHTMLFile, shlwapi/PathIsHTMLFile, shlwapi/PathIsHTMLFileA, shlwapi/PathIsHTMLFileW
ms.topic: macro
f1_keywords:
- shlwapi/PathIsHTMLFile
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
req.unicode-ansi: PathIsHTMLFileW (Unicode) and PathIsHTMLFileA (ANSI)
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
api_name:
- PathIsHTMLFile
- PathIsHTMLFileA
- PathIsHTMLFileW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsHTMLFileW macro


## -description


Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

The address of a character buffer that contains the path and name of the file.

