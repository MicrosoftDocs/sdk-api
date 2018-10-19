---
UID: NF:shlwapi.SHGetValueW
title: SHGetValueW function
author: windows-sdk-content
description: Retrieves a registry value.
old-location: shell\SHGetValue.htm
tech.root: shell
ms.assetid: 8cca6bfe-d365-4d10-bc8d-f3bebefaad02
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHGetValue, SHGetValue function [Windows Shell], SHGetValueA, SHGetValueW, _win32_SHGetValue, shell.SHGetValue, shlwapi/SHGetValue, shlwapi/SHGetValueA, shlwapi/SHGetValueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetValueW (Unicode) and SHGetValueA (ANSI)
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
 - SHGetValue
 - SHGetValueA
 - SHGetValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetValueW function


## -description


Retrieves a registry value.


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

The address of a null-terminated string that specifies the name of the subkey from which to retrieve the value.


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

The address of the value.


### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

The type of value. For more information, see <a href="https://msdn.microsoft.com/4185e7af-e1f0-40af-91c7-0ff7e27896ae">Registry Data Types</a>.


### -param pvData [out, optional]

Type: <b>LPVOID</b>

The address of the destination data buffer.


### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

The size of the destination data buffer.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -remarks



If your application must set/retrieve a series of values in the same key, it is better to open the key once and set/retrieve the values with the regular Microsoft Win32 registry functions rather than use this function repeatedly.



