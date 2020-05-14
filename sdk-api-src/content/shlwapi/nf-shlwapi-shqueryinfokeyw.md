---
UID: NF:shlwapi.SHQueryInfoKeyW
title: SHQueryInfoKeyW function (shlwapi.h)
description: Retrieves information about a specified registry key.helpviewer_keywords: ["HKEY_CLASSES_ROOT","HKEY_CURRENT_CONFIG","HKEY_CURRENT_USER","HKEY_LOCAL_MACHINE","HKEY_PERFORMANCE_DATA","HKEY_USERS","SHQueryInfoKey","SHQueryInfoKey function [Windows Shell]","SHQueryInfoKeyA","SHQueryInfoKeyW","_win32_SHQueryInfoKey","shell.SHQueryInfoKey","shlwapi/SHQueryInfoKey","shlwapi/SHQueryInfoKeyA","shlwapi/SHQueryInfoKeyW"]
old-location: shell\SHQueryInfoKey.htm
tech.root: shell
ms.assetid: dea535e7-5e61-4587-aa22-b1d62b76943a
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHQueryInfoKey, SHQueryInfoKey function [Windows Shell], SHQueryInfoKeyA, SHQueryInfoKeyW, _win32_SHQueryInfoKey, shell.SHQueryInfoKey, shlwapi/SHQueryInfoKey, shlwapi/SHQueryInfoKeyA, shlwapi/SHQueryInfoKeyW
f1_keywords:
- shlwapi/SHQueryInfoKey
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
req.unicode-ansi: SHQueryInfoKeyW (Unicode) and SHQueryInfoKeyA (ANSI)
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
- API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
- ShCore.dll
- API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
- API-MS-Win-ShCore-Registry-l1-1-0.dll
- API-MS-Win-ShCore-Registry-l1-1-1.dll
api_name:
- SHQueryInfoKey
- SHQueryInfoKeyA
- SHQueryInfoKeyW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHQueryInfoKeyW function


## -description


Retrieves information about a specified registry key.


## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

A handle to the currently open key, or any of the following predefined values.



#### HKEY_CLASSES_ROOT



#### HKEY_CURRENT_CONFIG



#### HKEY_CURRENT_USER



#### HKEY_LOCAL_MACHINE



#### HKEY_PERFORMANCE_DATA



#### HKEY_USERS


### -param pcSubKeys [out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that receives the number of subkeys under the specified key.


### -param pcchMaxSubKeyLen [out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that receives the number of characters in the name of the subkey with the largest name.


### -param pcValues [out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that receives the number of values under the specified key.


### -param pcchMaxValueNameLen [out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that receives the number of characters in the name of the value with the largest name.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.



