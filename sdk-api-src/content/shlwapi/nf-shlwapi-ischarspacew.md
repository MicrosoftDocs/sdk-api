---
UID: NF:shlwapi.IsCharSpaceW
title: IsCharSpaceW function (shlwapi.h)
description: Determines whether a character represents a space. (Unicode)
helpviewer_keywords: ["IsCharSpace", "IsCharSpace function [Windows Shell]", "IsCharSpaceW", "_shell_IsCharSpace", "shell.IsCharSpace", "shlwapi/IsCharSpace", "shlwapi/IsCharSpaceW"]
old-location: shell\IsCharSpace.htm
tech.root: shell
ms.assetid: 40ccde4d-38e8-4c03-a826-b6c060037ae5
ms.date: 12/05/2018
ms.keywords: IsCharSpace, IsCharSpace function [Windows Shell], IsCharSpaceA, IsCharSpaceW, _shell_IsCharSpace, shell.IsCharSpace, shlwapi/IsCharSpace, shlwapi/IsCharSpaceA, shlwapi/IsCharSpaceW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsCharSpaceW
 - shlwapi/IsCharSpaceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l1-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - IsCharSpace
 - IsCharSpaceA
 - IsCharSpaceW
---

# IsCharSpaceW function


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




> [!NOTE]
> The shlwapi.h header defines IsCharSpace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

