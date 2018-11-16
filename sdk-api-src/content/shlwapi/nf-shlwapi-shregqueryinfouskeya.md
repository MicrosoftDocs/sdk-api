---
UID: NF:shlwapi.SHRegQueryInfoUSKeyA
title: SHRegQueryInfoUSKeyA function
author: windows-sdk-content
description: Retrieves information about a specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegQueryInfoUSKey.htm
tech.root: shell
ms.assetid: e47b4fad-50c7-43d7-82f2-6a835ac543f0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SHRegQueryInfoUSKey, SHRegQueryInfoUSKey function [Windows Shell], SHRegQueryInfoUSKeyA, SHRegQueryInfoUSKeyW, _win32_SHRegQueryInfoUSKey, shell.SHRegQueryInfoUSKey, shlwapi/SHRegQueryInfoUSKey, shlwapi/SHRegQueryInfoUSKeyA, shlwapi/SHRegQueryInfoUSKeyW
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
req.unicode-ansi: SHRegQueryInfoUSKeyW (Unicode) and SHRegQueryInfoUSKeyA (ANSI)
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
api_name:
 - SHRegQueryInfoUSKey
 - SHRegQueryInfoUSKeyA
 - SHRegQueryInfoUSKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SHRegQueryInfoUSKeyA
: 
---

# SHRegQueryInfoUSKeyA function


## -description


Retrieves information about a specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


### -param pcSubKeys [out, optional]

Type: <b>LPDWORD</b>

A pointer to  a <b>DWORD</b> that receives the number of subkeys under the specified key.


### -param pcchMaxSubKeyLen [out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the number of characters in the largest subkey name.


### -param pcValues [out, optional]

Type: <b>LPDWORD</b>

A pointer to  a <b>DWORD</b> that receives the number of values under the specified key.


### -param pcchMaxValueNameLen [out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the number of characters in the largest value name.


### -param enumRegFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4216a983-9d53-44b1-8273-e5a90ac4b3ef">SHREGENUM_FLAGS</a></b>

One of the <a href="https://msdn.microsoft.com/4216a983-9d53-44b1-8273-e5a90ac4b3ef">SHREGENUM_FLAGS</a> that specifies the base key in which the query should take place.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.



