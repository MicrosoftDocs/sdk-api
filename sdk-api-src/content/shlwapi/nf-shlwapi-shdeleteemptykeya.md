---
UID: NF:shlwapi.SHDeleteEmptyKeyA
title: SHDeleteEmptyKeyA function
author: windows-sdk-content
description: Deletes an empty key.
old-location: shell\SHDeleteEmptyKey.htm
tech.root: shell
ms.assetid: 6a560bc3-f65e-4b7d-9fbc-b4f2971ce2a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHDeleteEmptyKey, SHDeleteEmptyKey function [Windows Shell], SHDeleteEmptyKeyA, SHDeleteEmptyKeyW, _win32_SHDeleteEmptyKey, shell.SHDeleteEmptyKey, shlwapi/SHDeleteEmptyKey, shlwapi/SHDeleteEmptyKeyA, shlwapi/SHDeleteEmptyKeyW
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHDeleteEmptyKeyW (Unicode) and SHDeleteEmptyKeyA (ANSI)
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
 - SHDeleteEmptyKey
 - SHDeleteEmptyKeyA
 - SHDeleteEmptyKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHDeleteEmptyKeyA function


## -description


Deletes an empty key.


## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

A handle to an open registry key, or one of the following <a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:

<a id="HKEY_CLASSES_ROOT"></a>
<a id="hkey_classes_root"></a>


#### HKEY_CLASSES_ROOT

<a id="HKEY_CURRENT_CONFIG"></a>
<a id="hkey_current_config"></a>


#### HKEY_CURRENT_CONFIG

<a id="HKEY_CURRENT_USER"></a>
<a id="hkey_current_user"></a>


#### HKEY_CURRENT_USER

<a id="HKEY_LOCAL_MACHINE"></a>
<a id="hkey_local_machine"></a>


#### HKEY_LOCAL_MACHINE

<a id="HKEY_PERFORMANCE_DATA"></a>
<a id="hkey_performance_data"></a>


#### HKEY_PERFORMANCE_DATA

<a id="HKEY_USERS"></a>
<a id="hkey_users"></a>


#### HKEY_USERS


### -param pszSubKey [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string specifying the name of the key to delete.


## -returns



Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to retrieve a generic description of the error.




## -remarks



<b>SHDeleteEmptyKey</b> does not delete a key if it contains any subkeys or values. Use <a href="https://msdn.microsoft.com/3c46db08-52d8-48fa-bda5-3c087908a1d3">SHDeleteKey</a> instead.

Alternatively, use the <a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a> or <a href="https://msdn.microsoft.com/984813a9-e191-498f-8288-b8a4c567112b">RegDeleteTree</a> function.



