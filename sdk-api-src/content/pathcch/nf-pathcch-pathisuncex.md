---
UID: NF:pathcch.PathIsUNCEx
title: PathIsUNCEx function (pathcch.h)
description: Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.This function differs from PathIsUNC in that it also allows you to extract the name of the server from the path.
helpviewer_keywords: ["PathIsUNCEx","PathIsUNCEx function [Windows Shell]","pathcch/PathIsUNCEx","shell.PathIsUNCEx"]
old-location: shell\PathIsUNCEx.htm
tech.root: shell
ms.assetid: 3b2a4158-63ec-49eb-a031-7493d02f2caa
ms.date: 12/05/2018
ms.keywords: PathIsUNCEx, PathIsUNCEx function [Windows Shell], pathcch/PathIsUNCEx, shell.PathIsUNCEx
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
 - PathIsUNCEx
 - pathcch/PathIsUNCEx
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
 - PathIsUNCEx
---

# PathIsUNCEx function


## -description

Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathisunca">PathIsUNC</a> in that it also allows you to extract the name of the server from the path.

## -parameters

### -param pszPath [in]

A pointer to the path string.

### -param ppszServer [out, optional]

A pointer to a string that, when this function returns successfully, receives the server portion of the UNC path. This value can be <b>NULL</b> if you don't need this information.

## -returns

Returns <b>TRUE</b> if the string is a valid UNC path; otherwise, <b>FALSE</b>.