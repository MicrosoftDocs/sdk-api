---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PathCchFindExtension function


## -description



Searches a path to find its file name extension, such as ".exe" or ".ini". This function does not search for a specific extension; it searches for the presence of any extension.

This function differs from <a href="https://msdn.microsoft.com/afebd4b7-2685-4b6e-8f8a-d43944dacef5">PathFindExtension</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/afebd4b7-2685-4b6e-8f8a-d43944dacef5">PathFindExtension</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in]

A pointer to the path to search.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


### -param ppszExt [out]

The address of a pointer that, when this function returns successfully, points to the "." character that precedes the extension within <i>pszPath</i>. If no extension is found, it points to the string's terminating null character.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



