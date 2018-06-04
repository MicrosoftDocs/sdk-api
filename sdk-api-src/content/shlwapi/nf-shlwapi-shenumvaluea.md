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

# SHEnumValueA function


## -description


Enumerates the values of the specified open registry key.


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


### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the value to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.


### -param pszValueName

Type: <b>LPTSTR</b>

The address of a character buffer that receives the enumerated value name. The size of this buffer is specified in <i>pcchValueName</i>.


### -param pcchValueName [in, out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pszValueName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszValueName</i>.


### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that receives the data type of the value. These are the same values as those described under the <i>lpType</i> parameter of <a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a>.


### -param pvData

Type: <b>LPVOID</b>

The address of a buffer that receives the data for the value entry. The size of this buffer is specified in <i>pcbData</i>. This parameter can be <b>NULL</b> if the data is not required.


### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

The address of a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pvData</i>, in bytes. On exit, this contains the number of bytes that were copied to <i>pvData</i>.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a textual description of the error.



