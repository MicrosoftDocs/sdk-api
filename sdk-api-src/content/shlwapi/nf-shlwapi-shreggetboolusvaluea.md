---
UID: NF:shlwapi.SHRegGetBoolUSValueA
title: SHRegGetBoolUSValueA function (shlwapi.h)
description: Retrieves a Boolean value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).helpviewer_keywords: ["SHRegGetBoolUSValue","SHRegGetBoolUSValue function [Windows Shell]","SHRegGetBoolUSValueA","SHRegGetBoolUSValueW","_win32_SHRegGetBoolUSValue","shell.SHRegGetBoolUSValue","shlwapi/SHRegGetBoolUSValue","shlwapi/SHRegGetBoolUSValueA","shlwapi/SHRegGetBoolUSValueW"]
old-location: shell\SHRegGetBoolUSValue.htm
tech.root: shell
ms.assetid: afd95ce4-0ced-48ce-814f-1d02d7913be5
ms.date: 12/05/2018
ms.keywords: SHRegGetBoolUSValue, SHRegGetBoolUSValue function [Windows Shell], SHRegGetBoolUSValueA, SHRegGetBoolUSValueW, _win32_SHRegGetBoolUSValue, shell.SHRegGetBoolUSValue, shlwapi/SHRegGetBoolUSValue, shlwapi/SHRegGetBoolUSValueA, shlwapi/SHRegGetBoolUSValueW
f1_keywords:
- shlwapi/SHRegGetBoolUSValue
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegGetBoolUSValueW (Unicode) and SHRegGetBoolUSValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shlwapi.dll
- API-MS-Win-Core-Registryuserspecific-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
- SHRegGetBoolUSValue
- SHRegGetBoolUSValueA
- SHRegGetBoolUSValueW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHRegGetBoolUSValueA function


## -description


Retrieves a Boolean value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param pszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the subkey relative to <b>HKEY_LOCAL_MACHINE</b> and <b>HKEY_CURRENT_USER</b>. For example, "Software\MyCompany\MyProduct".


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the name of the value. This value can be <b>NULL</b>.


### -param fIgnoreHKCU [in]

Type: <b>BOOL</b>

A variable that specifies which key to look under. When set to <b>TRUE</b>, <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea">SHRegGetUSValue</a> ignores <b>HKEY_CURRENT_USER</b> and returns a value from <b>HKEY_LOCAL_MACHINE</b>.


### -param fDefault [in]

Type: <b>BOOL</b>

A value that is returned if there is no registry value.


## -returns



Type: <b>BOOL</b>

Returns either the value from the registry, or <i>fDefault</i> if none is found.



