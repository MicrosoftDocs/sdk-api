---
UID: NF:shlwapi.SHEnumKeyExW
title: SHEnumKeyExW function (shlwapi.h)
author: windows-sdk-content
description: Enumerates the subkeys of the specified open registry key.
old-location: shell\SHEnumKeyEx.htm
tech.root: shell
ms.assetid: 51bf9cf7-87bc-407c-b2ee-18db3cdfe1dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHEnumKeyEx, SHEnumKeyEx function [Windows Shell], SHEnumKeyExA, SHEnumKeyExW, _win32_SHEnumKeyEx, shell.SHEnumKeyEx, shlwapi/SHEnumKeyEx, shlwapi/SHEnumKeyExA, shlwapi/SHEnumKeyExW
ms.topic: function
f1_keywords: 
 - "shlwapi/SHEnumKeyEx"
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHEnumKeyExW (Unicode) and SHEnumKeyExA (ANSI)
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
 - SHEnumKeyEx
 - SHEnumKeyExA
 - SHEnumKeyExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHEnumKeyExW function


## -description


Enumerates the subkeys of the specified open registry key.


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


### -param dwIndex

Type: <b>DWORD</b>

The index of the subkey to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.


### -param pszName

Type: <b>LPTSTR</b>

The address of a character buffer that receives the enumerated key name.


### -param pcchName [in]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pszName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszName</i>.


##### - hkey.HKEY_CLASSES_ROOT


##### - hkey.HKEY_CURRENT_CONFIG


##### - hkey.HKEY_CURRENT_USER


##### - hkey.HKEY_LOCAL_MACHINE


##### - hkey.HKEY_PERFORMANCE_DATA


##### - hkey.HKEY_USERS


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.



