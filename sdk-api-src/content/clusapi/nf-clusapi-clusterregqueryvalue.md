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

# ClusterRegQueryValue function


## -description


Returns the 
    name, type, and data components associated with a value for an open 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle of the cluster database key to query.


### -param lpszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to be queried.


### -param lpdwValueType [out, optional]

Pointer to the key's value type. This parameter can be <b>NULL</b> if the type is not 
       required; otherwise, the value returned through this parameter is one of the following.



#### REG_BINARY (3)

Binary data in any form.



#### REG_DWORD (4)

A 32-bit number.



#### REG_DWORD_BIG_ENDIAN (5)

A 32-bit number stored in big-endian format.



#### REG_EXPAND_SZ (2)

A null-terminated Unicode string that contains unexpanded references to environment variables (for example, 
         "%PATH%").



#### REG_MULTI_SZ (6)

A sequence of null-terminated strings, terminated by an empty string (\0).

The following is an example:

<i>String1</i>\0<i>String2</i>\0<i>String3</i>\0<i>LastString</i>\0\0

The first \0 terminates the first string, the second to the last \0 terminates the last string, and the 
         final \0 terminates the sequence. Note that the final terminator must be factored into the length of the 
         string.



#### REG_NONE (0)

No defined value type.



#### REG_QWORD (11)

A 64-bit number.



#### REG_SZ (1)

A null-terminated Unicode string.


### -param lpData [out, optional]

Pointer to the value's data. This parameter can be <b>NULL</b> if the data is not 
       required.


### -param lpcbData [in, out, optional]

On input, pointer to the count of bytes in the buffer pointed to by the <i>lpbData</i> 
       parameter. On output, pointer to the count of bytes in the value's data, which is placed in the content of 
       <i>lpbData</i> if the caller passes in a valid pointer.

The <i>lpbData</i> parameter can be <b>NULL</b> only if 
       <i>lpbData</i> is also <b>NULL</b>.


## -returns



The function returns one of the following values.




## -remarks



If <i>lpbData</i> is <b>NULL</b>, the 
     <b>ClusterRegQueryValue</b> function returns <b>ERROR_SUCCESS</b> 
     and stores the size of the value's data in the content of <i>lpbData</i>. This information 
     allows the caller to correctly allocate a buffer to hold the data.

If <i>lpdwValueType</i> is set to <b>REG_SZ</b>, 
     <b>REG_MULTI_SZ</b> or <b>REG_EXPAND_SZ</b>, then 
     <i>lpbData</i> also includes a <b>NULL</b> terminator.




## -see-also




<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>
 

 

