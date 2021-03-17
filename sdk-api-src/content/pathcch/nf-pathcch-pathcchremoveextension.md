---
UID: NF:pathcch.PathCchRemoveExtension
title: PathCchRemoveExtension function (pathcch.h)
description: Removes the file name extension from a path, if one is present.This function differs from PathRemoveExtension in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PathCchRemoveExtension","PathCchRemoveExtension function [Windows Shell]","pathcch/PathCchRemoveExtension","shell.PathCchRemoveExtension"]
old-location: shell\PathCchRemoveExtension.htm
tech.root: shell
ms.assetid: 9adfb054-6d62-41bb-9036-0bf670ea24b2
ms.date: 12/05/2018
ms.keywords: PathCchRemoveExtension, PathCchRemoveExtension function [Windows Shell], pathcch/PathCchRemoveExtension, shell.PathCchRemoveExtension
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
 - PathCchRemoveExtension
 - pathcch/PathCchRemoveExtension
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
 - PathCchRemoveExtension
---

# PathCchRemoveExtension function


## -description

Removes the file name extension from a path, if one is present.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremoveextensiona">PathRemoveExtension</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>This function, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremoveextensiona">PathRemoveExtension</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any extension removed. If no extension was found, the string is unchanged.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

## -returns

This function returns <b>S_OK</b> if the function was successful, <b>S_FALSE</b> if no extension was found, or an error code otherwise.