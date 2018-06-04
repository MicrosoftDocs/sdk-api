---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHRegSetUSValueW function


## -description


Sets a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param pwzSubKey

TBD


### -param pwzValue

TBD


### -param dwType [in]

Type: <b>DWORD</b>

Type of data to be stored. This parameter must be the <b>REG_SZ</b> type. For more information, see <a href="https://msdn.microsoft.com/4185e7af-e1f0-40af-91c7-0ff7e27896ae">Registry Data Types</a>.


### -param pvData [in, optional]

Type: <b>LPVOID*</b>

 Apointer to a null-terminated string that contains the value to be set for the specified key.


### -param cbData [in, optional]

Type: <b>DWORD</b>

Length, in bytes, of the string pointed to by the <i>pvData</i> parameter, not including the terminating null character.


### -param dwFlags [in, optional]

Type: <b>DWORD</b>

Flags indicating where the data should be written.



#### SHREGSET_HKCU

Write to <b>HKEY_CURRENT_USER</b> if empty.



#### SHREGSET_FORCE_HKCU

Write to <b>HKEY_CURRENT_USER</b>.



#### SHREGSET_HKLM

Write to <b>HKEY_LOCAL_MACHINE</b> if empty.



#### SHREGSET_FORCE_HKLM

Write to <b>HKEY_LOCAL_MACHINE</b>.



#### SHREGSET_DEFAULT

Equivalent to (<b>SHREGSET_FORCE_HKCU</b> | <b>SHREGSET_HKLM</b>).


##### - dwFlags.SHREGSET_DEFAULT

Equivalent to (<b>SHREGSET_FORCE_HKCU</b> | <b>SHREGSET_HKLM</b>).


##### - dwFlags.SHREGSET_FORCE_HKCU

Write to <b>HKEY_CURRENT_USER</b>.


##### - dwFlags.SHREGSET_FORCE_HKLM

Write to <b>HKEY_LOCAL_MACHINE</b>.


##### - dwFlags.SHREGSET_HKCU

Write to <b>HKEY_CURRENT_USER</b> if empty.


##### - dwFlags.SHREGSET_HKLM

Write to <b>HKEY_LOCAL_MACHINE</b> if empty.


#### - pszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the subkey.


#### - pszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the name of the value.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -remarks



This function opens the key each time it is used. If your code involves setting a series of values in the same key, it is more efficient to open the key once with <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> and then use <a href="https://msdn.microsoft.com/f94569c6-415b-4263-bab4-8a5baca47901">SHRegWriteUSValue</a> to write the data.



