---
UID: NF:shlwapi.SHSetValueA
title: SHSetValueA function
author: windows-sdk-content
description: Sets the value of a registry key.
old-location: shell\SHSetValue.htm
old-project: shell
ms.assetid: 6cd5b7fd-8fb9-4c24-9670-20c23ca709bf
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHSetValue, SHSetValue function [Windows Shell], SHSetValueA, SHSetValueW, _win32_SHSetValue, shell.SHSetValue, shlwapi/SHSetValue, shlwapi/SHSetValueA, shlwapi/SHSetValueW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: URL_SCHEME
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
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHSetValueA function


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

Type of data to be stored. This parameter must be the <b>REG_SZ</b> type. For more information, see <a href="https://msdn.microsoft.com/4185e7af-e1f0-40af-91c7-0ff7e27896ae">Registry Data Types</a>.


### -param pvData [in, optional]

Type: <b>LPCVOID</b>

Pointer to a buffer that contains the data to set for the specified value. This value can be <b>NULL</b>.


### -param cbData [in]

Type: <b>DWORD</b>

Length, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. If the data is a null-terminated string, this length includes the terminating null character.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful; otherwise, a nonzero error code defined in Winerror.h. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.



