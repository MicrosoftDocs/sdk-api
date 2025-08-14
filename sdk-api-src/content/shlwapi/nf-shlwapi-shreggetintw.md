---
UID: NF:shlwapi.SHRegGetIntW
title: SHRegGetIntW function (shlwapi.h)
description: Reads a numeric string value from the registry and converts it to an integer.
helpviewer_keywords: ["SHRegGetIntW","SHRegGetIntW function [Windows Shell]","_shell_SHRegGetInt","shell.SHRegGetInt","shlwapi/SHRegGetIntW"]
old-location: shell\SHRegGetInt.htm
tech.root: shell
ms.assetid: 027e3470-46be-4d37-b815-e1fd550d0c60
ms.date: 12/05/2018
ms.keywords: SHRegGetIntW, SHRegGetIntW function [Windows Shell], _shell_SHRegGetInt, shell.SHRegGetInt, shlwapi/SHRegGetIntW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegGetIntW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRegGetIntW
 - shlwapi/SHRegGetIntW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l2-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - ShCore.dll
 - API-MS-Win-ShCore-Registry-l1-1-0.dll
 - API-MS-Win-ShCore-Registry-l1-1-1.dll
api_name:
 - SHRegGetIntW
 - SHRegGetIntW
---

# SHRegGetIntW function


## -description

Reads a numeric string value from the registry and converts it to an integer.

## -parameters

### -param hk [in]

Type: <b>HKEY</b>

A handle to the registry key that specifies the value to be read.

### -param pwzKey [in]

Type: <b>LPCWSTR</b>

A pointer to a string value that specifies the name of the value to be read. The string must be null-terminated.

### -param iDefault [in]

Type: <b>int</b>

An <b>int</b> that specifies the value returned if the registry value cannot be retrieved successfully.

## -returns

Type: <b>int</b>

Returns the converted string as an <b>int</b>, or the default value specified by <i>nDefault</i>.

## -remarks

Prior to Windows 2000 Service Pack 3 (SP3), Windows Server 2003 Service Pack 1 (SP1), and Windows XP, <b>SHRegGetIntW</b> was not exported by name. On those systems you must load it directly from Shlwapi.dll as ordinal 280.

This function is only available in a Unicode version. ANSI is not supported.

