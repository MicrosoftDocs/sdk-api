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

# SHRegQueryInfoUSKeyW function


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



