---
UID: NF:shlwapi.SHRegEnumUSKeyA
title: SHRegEnumUSKeyA function
author: windows-sdk-content
description: Enumerates the subkeys of a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegEnumUSKey.htm
tech.root: shell
ms.assetid: 9418ad45-f451-4976-afd7-fa1e0088038d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: SHRegEnumUSKey, SHRegEnumUSKey function [Windows Shell], SHRegEnumUSKeyA, SHRegEnumUSKeyW, _win32_SHRegEnumUSKey, shell.SHRegEnumUSKey, shlwapi/SHRegEnumUSKey, shlwapi/SHRegEnumUSKeyA, shlwapi/SHRegEnumUSKeyW
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
req.unicode-ansi: SHRegEnumUSKeyW (Unicode) and SHRegEnumUSKeyA (ANSI)
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
 - SHRegEnumUSKey
 - SHRegEnumUSKeyA
 - SHRegEnumUSKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHRegEnumUSKeyA function


## -description


Enumerates the subkeys of a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the subkey to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.


### -param pszName

TBD


### -param pcchName [in, out]

Type: <b>LPDWORD</b>

A pointer to  a DWORD that, on entry, contains the size of the buffer at <i>pszName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszName</i>.


### -param enumRegFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4216a983-9d53-44b1-8273-e5a90ac4b3ef">SHREGENUM_FLAGS</a></b>

A <a href="https://msdn.microsoft.com/4216a983-9d53-44b1-8273-e5a90ac4b3ef">SHREGENUM_FLAGS</a> that specifies the base key in which the enumeration should take place.


#### - pwzName [out]

Type: <b>LPTSTR</b>

A pointer to a character buffer that receives the enumerated key name.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.



