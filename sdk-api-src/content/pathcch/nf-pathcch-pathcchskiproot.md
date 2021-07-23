---
UID: NF:pathcch.PathCchSkipRoot
title: PathCchSkipRoot function (pathcch.h)
description: Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.This function differs from PathSkipRoot in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PathCchSkipRoot","PathCchSkipRoot function [Windows Shell]","pathcch/PathCchSkipRoot","shell.PathCchSkipRoot"]
old-location: shell\PathCchSkipRoot.htm
tech.root: shell
ms.assetid: 187bc49e-c5ae-42b8-acbd-a765f871d73b
ms.date: 12/05/2018
ms.keywords: PathCchSkipRoot, PathCchSkipRoot function [Windows Shell], pathcch/PathCchSkipRoot, shell.PathCchSkipRoot
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pathcch.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathCchSkipRoot
 - pathcch/PathCchSkipRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - pathcch.lib
 - API-MS-Win-Core-Path-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PathCchSkipRoot
---

# PathCchSkipRoot function


## -description

Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathskiproota">PathSkipRoot</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

## -parameters

### -param pszPath [in]

A pointer to the path string.

### -param ppszRootEnd [out]

The address of a pointer that, when this function returns successfully, points to the first character in a path following the drive letter or UNC server/share path elements. If the path consists of only a root, this value will point to the string's terminating null character.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.