---
UID: NF:pathcch.PathCchFindExtension
title: PathCchFindExtension function
author: windows-driver-content
description: Searches a path to find its file name extension, such as &#0034;.exe&#0034; or &#0034;.ini&#0034;.
old-location: shell\PathCchFindExtension.htm
old-project: shell
ms.assetid: dac6cf02-7b53-449c-b788-4a7b6d1622ed
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: PathCchFindExtension, PathCchFindExtension function [Windows Shell], pathcch/PathCchFindExtension, shell.PathCchFindExtension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	pathcch.lib
-	API-MS-Win-Core-Path-l1-1-0.dll
-	KernelBase.dll
api_name:
-	PathCchFindExtension
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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



