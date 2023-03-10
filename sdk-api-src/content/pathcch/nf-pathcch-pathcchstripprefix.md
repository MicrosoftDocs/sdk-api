---
UID: NF:pathcch.PathCchStripPrefix
title: PathCchStripPrefix function (pathcch.h)
description: Removes the &quot;\\?\&quot; prefix, if present, from a file path.
helpviewer_keywords: ["PathCchStripPrefix","PathCchStripPrefix function [Windows Shell]","pathcch/PathCchStripPrefix","shell.PathCchStripPrefix"]
old-location: shell\PathCchStripPrefix.htm
tech.root: shell
ms.assetid: 2e50b23e-2725-4200-bd5e-845ff3458026
ms.date: 12/05/2018
ms.keywords: PathCchStripPrefix, PathCchStripPrefix function [Windows Shell], pathcch/PathCchStripPrefix, shell.PathCchStripPrefix
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
 - PathCchStripPrefix
 - pathcch/PathCchStripPrefix
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
 - PathCchStripPrefix
---

# PathCchStripPrefix function


## -description

Removes the "\\?\" prefix, if present, from a file path.

## -parameters

### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the same path string will have had the prefix removed, if the prefix was present. If no prefix was present, the string will be unchanged.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

## -returns

This function returns <b>S_OK</b> if the prefix was removed, <b>S_FALSE</b> if the path did not have a prefix to remove, or an <b>HRESULT</b> failure code.

