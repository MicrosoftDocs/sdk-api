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

# SHRegCreateUSKeyW function


## -description


Creates or opens a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param pwzPath

TBD


### -param samDesired [in]

Type: <b><a href="https://msdn.microsoft.com/003f6be9-e4ba-4d23-b486-a167063c630e">REGSAM</a></b>

The desired security access. For more information on security access, see <a href="https://msdn.microsoft.com/003f6be9-e4ba-4d23-b486-a167063c630e">REGSAM</a>.


### -param hRelativeUSKey [in, optional]

Type: <b>HUSKEY</b>

The key to be used as a base for relative paths. If <i>pszPath</i> is a relative path, the key it specifies will be relative to <i>hRelativeUSKey</i>. If <i>pszPath</i> is an absolute path, set <i>hRelativeUSKey</i> to <b>NULL</b>. The key will then be created under <b>HKEY_LOCAL_MACHINE</b> or <b>HKEY_CURRENT_USER</b>, depending the value of <i>dwFlags</i>.


### -param phNewUSKey [out]

Type: <b>PHUSKEY</b>

A pointer to an <b>HUSKEY</b> that will receive the handle to the new key.


### -param dwFlags [in]

Type: <b>DWORD</b>

The base key under which the key should be opened. This can be one or more of the following values.



#### SHREGSET_HKCU

Create/open the key under <b>HKEY_CURRENT_USER</b>. Only creates a key if it is empty.



#### SHREGSET_FORCE_HKCU

Create/open the key under <b>HKEY_CURRENT_USER</b>. Creates a key even if it is not empty.



#### SHREGSET_HKLM

Create/open the key under <b>HKEY_LOCAL_MACHINE</b>. Only creates a key if it is empty.



#### SHREGSET_FORCE_HKLM

Create/open the key under <b>HKEY_LOCAL_MACHINE</b>. Creates a key even if it is not empty.



#### SHREGSET_DEFAULT

Create/open the key under both <b>HKEY_CURRENT_USER</b> (forced) and <b>HKEY_LOCAL_MACHINE</b> (only if empty). This flag is the equivalent of (<b>SHREGSET_FORCE_HKCU</b> | <b>SHREGSET_HKLM</b>).


##### - dwFlags.SHREGSET_DEFAULT

Create/open the key under both <b>HKEY_CURRENT_USER</b> (forced) and <b>HKEY_LOCAL_MACHINE</b> (only if empty). This flag is the equivalent of (<b>SHREGSET_FORCE_HKCU</b> | <b>SHREGSET_HKLM</b>).


##### - dwFlags.SHREGSET_FORCE_HKCU

Create/open the key under <b>HKEY_CURRENT_USER</b>. Creates a key even if it is not empty.


##### - dwFlags.SHREGSET_FORCE_HKLM

Create/open the key under <b>HKEY_LOCAL_MACHINE</b>. Creates a key even if it is not empty.


##### - dwFlags.SHREGSET_HKCU

Create/open the key under <b>HKEY_CURRENT_USER</b>. Only creates a key if it is empty.


##### - dwFlags.SHREGSET_HKLM

Create/open the key under <b>HKEY_LOCAL_MACHINE</b>. Only creates a key if it is empty.


#### - pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the subkey to be created or opened. If a value with this name is already present in the subkey, it will be opened.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -remarks



If you want to write values to the new key, use <a href="https://msdn.microsoft.com/f94569c6-415b-4263-bab4-8a5baca47901">SHRegWriteUSValue</a> to write each value, passing the <b>HUSKEY</b> handle that is returned through <i>phNewUSKey</i>. When you have finished, close the user-specific registry key with <a href="https://msdn.microsoft.com/1e9900d6-8411-4e6b-a9c0-006f378a2625">SHRegCloseUSKey</a>.



