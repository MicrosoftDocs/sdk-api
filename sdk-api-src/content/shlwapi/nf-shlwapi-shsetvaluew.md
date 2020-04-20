---
UID: NF:shlwapi.SHSetValueW
title: SHSetValueW function (shlwapi.h)
description: Sets the value of a registry key.helpviewer_keywords: ["HKEY_CLASSES_ROOT","HKEY_CURRENT_CONFIG","HKEY_CURRENT_USER","HKEY_LOCAL_MACHINE","HKEY_PERFORMANCE_DATA","HKEY_USERS","SHSetValue","SHSetValue function [Windows Shell]","SHSetValueA","SHSetValueW","_win32_SHSetValue","shell.SHSetValue","shlwapi/SHSetValue","shlwapi/SHSetValueA","shlwapi/SHSetValueW"]
old-location: shell\SHSetValue.htm
tech.root: shell
ms.assetid: 6cd5b7fd-8fb9-4c24-9670-20c23ca709bf
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHSetValue, SHSetValue function [Windows Shell], SHSetValueA, SHSetValueW, _win32_SHSetValue, shell.SHSetValue, shlwapi/SHSetValue, shlwapi/SHSetValueA, shlwapi/SHSetValueW
f1_keywords:
- shlwapi/SHSetValue
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
req.unicode-ansi: SHSetValueW (Unicode) and SHSetValueA (ANSI)
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
- SHSetValue
- SHSetValueA
- SHSetValueW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHSetValueW function


## -description


Sets the value of a registry key.


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


### -param pszSubKey [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies the name of the subkey with which a value is associated. This can be <b>NULL</b> or a pointer to an empty string. In this case, the value is added to the key identified by the <i>hkey</i> parameter.


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies the value. This value can be <b>NULL</b>.


### -param dwType [in]

Type: <b>DWORD</b>

Type of data to be stored. This parameter must be the <b>REG_SZ</b> type. For more information, see <a href="https://docs.microsoft.com/windows/desktop/shell/schemas">Registry Data Types</a>.


### -param pvData [in, optional]

Type: <b>LPCVOID</b>

Pointer to a buffer that contains the data to set for the specified value. This value can be <b>NULL</b>.


### -param cbData [in]

Type: <b>DWORD</b>

Length, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. If the data is a null-terminated string, this length includes the terminating null character.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful; otherwise, a nonzero error code defined in Winerror.h. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.



