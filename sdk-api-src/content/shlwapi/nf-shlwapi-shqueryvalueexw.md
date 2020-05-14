---
UID: NF:shlwapi.SHQueryValueExW
title: SHQueryValueExW function (shlwapi.h)
description: Opens a registry key and queries it for a specific value.helpviewer_keywords: ["HKEY_CLASSES_ROOT","HKEY_CURRENT_CONFIG","HKEY_CURRENT_USER","HKEY_LOCAL_MACHINE","HKEY_PERFORMANCE_DATA","HKEY_USERS","SHQueryValueEx","SHQueryValueEx function [Windows Shell]","SHQueryValueExA","SHQueryValueExW","_win32_SHQueryValueEx","shell.SHQueryValueEx","shlwapi/SHQueryValueEx","shlwapi/SHQueryValueExA","shlwapi/SHQueryValueExW"]
old-location: shell\SHQueryValueEx.htm
tech.root: shell
ms.assetid: 9969acae-5965-40fe-bde9-6de9ddf26bb8
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHQueryValueEx, SHQueryValueEx function [Windows Shell], SHQueryValueExA, SHQueryValueExW, _win32_SHQueryValueEx, shell.SHQueryValueEx, shlwapi/SHQueryValueEx, shlwapi/SHQueryValueExA, shlwapi/SHQueryValueExW
f1_keywords:
- shlwapi/SHQueryValueEx
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
req.unicode-ansi: SHQueryValueExW (Unicode) and SHQueryValueExA (ANSI)
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
- SHQueryValueEx
- SHQueryValueExA
- SHQueryValueExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHQueryValueExW function


## -description


Opens a registry key and queries it for a specific value.


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


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

The address of the <b>null</b>-terminated string that contains the name of the value to be queried.


### -param pdwReserved

Type: <b>LPDWORD</b>

Reserved. Must be <b>NULL</b>.


### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

The address of the variable that receives the key's value type. For more information, see <a href="https://docs.microsoft.com/windows/desktop/shell/schemas">Registry Data Types</a>.


### -param pvData [out, optional]

Type: <b>LPVOID</b>

The address of the buffer that receives the value's data. This parameter can be <b>NULL</b> if the data is not required.


### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

The address of the variable that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, this variable contains the size of the data copied to <i>pvData</i>.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.



