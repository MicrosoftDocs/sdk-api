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

# SHRegGetValueFromHKCUHKLM function


## -description


<p class="CCE_Message">[This function is no longer supported.]

Obtains specified information from the registry. This function will check HKEY_CURRENT_USER for the requested information in the specified subkey. If the information does not exist under the HKEY_CURRENT_USER subtree, the function checks the HKEY_LOCAL_MACHINE subtree for the same information.

            


## -parameters




### -param pwszKey [in]

Type: <b>PCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the path to the registry key.


### -param pwszValue [in]

Type: <b>PCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the key value. This value can be <b>NULL</b>, in which case data is retrieved from the Default value.


### -param srrfFlags [in]

Type: <b><a href="https://msdn.microsoft.com/c9dbffd1-3b3e-4a25-89ee-1666e2812a62">SRRF</a></b>

The <a href="https://msdn.microsoft.com/c9dbffd1-3b3e-4a25-89ee-1666e2812a62">SRRF</a> flag constants. If more than one flag is used they can be combined using a bitwise OR. These flags are used to restrict the type of data returned. This value cannot be 0.


### -param pdwType [out]

Type: <b>DWORD*</b>

When this function returns, contains a pointer to a <b>DWORD</b> which receives a code that indicates the type of data stored in the specified value.  This can be set to <b>NULL</b> if no type information is wanted. If this value is not <b>NULL</b>, and the SRRF_NOEXPAND flag has not been set, data types of REG_EXPAND_SZ will be returned as REG_SZ since they are automatically expanded in this method.


### -param pvData [in]

Type: <b>LPCVOID</b>

A pointer to a buffer that contains the value's data. This parameter can be <b>NULL</b> if the data is not needed. This value must contain the size of the <i>pvData</i> buffer on entry.  If <i>pvData</i> is <b>NULL</b> (or if <i>pvData</i> is not <b>NULL</b>, but too small of a buffer to hold the registry data), then on exit it will contain the size required to hold the registry data.


### -param pcbData [in, out]

Type: <b>DWORD*</b>

When this function returns, contains a pointer to the size of the data, in bytes.


## -returns



Type: <b>LONG</b>

If successful, this function returns ERROR_SUCCESS and all out parameters requested. Returns ERROR_MORE_DATA if the function fails due to insufficient space in a provided non-<b>NULL</b> pvData. In this case  only <i>pdwType</i> and <i>pcbData</i> may contain valid data, <i>pvData</i> will be undefined. Otherwise, returns a nonzero error code defined in Winerror.h . You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.



