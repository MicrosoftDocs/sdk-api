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

# SHCopyKeyA function


## -description


Recursively copies the subkeys and values of the source subkey to the destination key. <b>SHCopyKey</b> does not copy the security attributes of the keys.


## -parameters




### -param hkeySrc [in]

Type: <b>HKEY</b>

A handle to the source key (for example, <b>HKEY_CURRENT_USER</b>).


### -param pszSrcSubKey [in, optional]

Type: <b>LPCTSTR</b>

The subkey whose subkeys and values are to be copied.


### -param hkeyDest [in]

Type: <b>HKEY</b>

The destination key.


### -param fReserved

Type: <b>DWORD</b>

Reserved. Must be 0.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or one of the nonzero error codes defined in Winerror.h otherwise. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -remarks



<div class="alert"><b>Important</b>  This function does not duplicate the security attributes of the keys and values that it copies. Rather, all security attributes in the destination key are the default attributes.</div>
<div> </div>


