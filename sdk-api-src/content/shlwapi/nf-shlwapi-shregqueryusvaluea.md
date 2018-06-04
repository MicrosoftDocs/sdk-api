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

# SHRegQueryUSValueA function


## -description


Retrieves the type and data for a specified name associated with an open registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey, or one of the following predefined values. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.



#### HKEY_CLASSES_ROOT



#### HKEY_CURRENT_CONFIG



#### HKEY_CURRENT_USER



#### HKEY_LOCAL_MACHINE



#### HKEY_PERFORMANCE_DATA



#### HKEY_USERS


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

A pointer to the <b>null</b>-terminated string that contains the name of the value to be queried.


### -param pdwType [in, out, optional]

Type: <b>LPDWORD*</b>

A pointer to the variable that sets or receives the key's value type. For more information, see <a href="https://msdn.microsoft.com/4185e7af-e1f0-40af-91c7-0ff7e27896ae">Registry Data Types</a>. This parameter can be <b>NULL</b>.


### -param pvData [out, optional]

Type: <b>LPVOID*</b>

A pointer to the buffer that receives the value's data. This parameter can be <b>NULL</b> if the data is not required.


### -param pcbData [in, out]

Type: <b>LPDWORD*</b>

A pointer to  the variable that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, this variable contains the size of the data copied to <i>pvData</i>.


### -param fIgnoreHKCU [in]

Type: <b>BOOL</b>

The variable that specifies which key to look under. When set to <b>TRUE</b>, <b>SHRegQueryUSValue</b> ignores <b>HKEY_CURRENT_USER</b> and returns the value from the key under <b>HKEY_LOCAL_MACHINE</b>.


### -param pvDefaultData [in, optional]

Type: <b>LPVOID*</b>

A pointer to the default data.


### -param dwDefaultDataSize [in, optional]

Type: <b>DWORD</b>

The length, in bytes, of the default data.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -remarks



When <i>fIgnoreHKCU</i> is set to <b>TRUE</b>, <b>SHRegQueryUSValue</b> returns the value from the key under <b>HKEY_LOCAL_MACHINE</b>. When set to <b>FALSE</b>, <b>SHRegQueryUSValue</b> first tries to return the value from the key under <b>HKEY_CURRENT_USER</b>. However, if the key is not found under <b>HKEY_CURRENT_USER</b>, the value returns from the key under <b>HKEY_LOCAL_MACHINE</b>. If neither key is present, or if an error occurs and <i>dwDefaultDataSize</i> is nonzero, then the default data is copied to <i>pvData</i> and ERROR_SUCCESS returns. ERROR_SUCCESS returns for both default and non-default data, and there is no way of distinguishing which value copies to <i>pvData</i>. To prevent the use of default data, set <i>pvDefaultData</i> to <b>NULL</b> and <i>dwDefaultDataSize</i> to zero.

If you only need to read a single value, <a href="https://msdn.microsoft.com/4d3b3bbe-dc2e-40c9-8ff1-0f9d2e323743">SHRegGetUSValue</a> will both open the key and return the value. To use <b>SHRegQueryUSValue</b>, you must first open the key with <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a>. However, once the key is opened, you can use <b>SHRegQueryUSValue</b> as many times as necessary. If you need to retrieve more than one value from the same key, using multiple calls to <b>SHRegQueryUSValue</b> is usually more efficient than <b>SHRegGetUSValue</b>, as the key is only opened once.



