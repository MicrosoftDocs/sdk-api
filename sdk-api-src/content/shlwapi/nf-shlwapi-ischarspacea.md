---
UID: NF:shlwapi.IsCharSpaceA
title: IsCharSpaceA function (shlwapi.h)
description: Determines whether a character represents a space.helpviewer_keywords: ["IsCharSpace","IsCharSpace function [Windows Shell]","IsCharSpaceA","IsCharSpaceW","_shell_IsCharSpace","shell.IsCharSpace","shlwapi/IsCharSpace","shlwapi/IsCharSpaceA","shlwapi/IsCharSpaceW"]
old-location: shell\IsCharSpace.htm
tech.root: shell
ms.assetid: 40ccde4d-38e8-4c03-a826-b6c060037ae5
ms.date: 12/05/2018
ms.keywords: IsCharSpace, IsCharSpace function [Windows Shell], IsCharSpaceA, IsCharSpaceW, _shell_IsCharSpace, shell.IsCharSpace, shlwapi/IsCharSpace, shlwapi/IsCharSpaceA, shlwapi/IsCharSpaceW
f1_keywords:
- shlwapi/IsCharSpace
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsCharSpaceW (Unicode) and IsCharSpaceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
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
- API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
- IsCharSpace
- IsCharSpaceA
- IsCharSpaceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsCharSpaceA function


## -description


Determines whether a character represents a space.


## -parameters




### -param wch [in]

Type: <b>TCHAR</b>

A single character.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the character is a space; otherwise, <b>FALSE</b>.




## -remarks



For those versions of Windows that do not include <b>IsCharSpace</b> in Shlwapi.h, <b>IsCharSpaceW</b> must be called directly from Shlwapi.dll (ordinal 29), using a WCHAR in the <i>wch</i> parameter. <b>IsCharSpaceA</b> is not available in versions of Windows that do not include <b>IsCharSpace</b> in Shlwapi.h.



