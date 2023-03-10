---
UID: NF:shlobj_core.PathGetShortPath
title: PathGetShortPath function (shlobj_core.h)
description: PathGetShortPath may be altered or unavailable.
helpviewer_keywords: ["PathGetShortPath","PathGetShortPath function [Windows Shell]","_win32_PathGetShortPath","shell.PathGetShortPath","shlobj_core/PathGetShortPath"]
old-location: shell\PathGetShortPath.htm
tech.root: shell
ms.assetid: f374a575-3fbf-4bed-aa76-76ed81e01d60
ms.date: 12/05/2018
ms.keywords: PathGetShortPath, PathGetShortPath function [Windows Shell], _win32_PathGetShortPath, shell.PathGetShortPath, shlobj_core/PathGetShortPath
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathGetShortPath
 - shlobj_core/PathGetShortPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - PathGetShortPath
---

# PathGetShortPath function


## -description

<p class="CCE_Message">[<b>PathGetShortPath</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the short path form of a specified input path.

## -parameters

### -param pszLongPath [in, out]

Type: <b>PWSTR</b>

A pointer to a null-terminated, Unicode string that contains the long path. When the function returns, it contains the equivalent short path.

