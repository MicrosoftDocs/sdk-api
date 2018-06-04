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

# BCryptEnumProviders function


## -description


The <b>BCryptEnumProviders</b> function obtains all of the CNG providers that support a specified algorithm.


## -parameters




### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that identifies the algorithm to obtain the providers for. This can be one of the predefined <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> or another algorithm identifier.


### -param pImplCount [out]

A pointer to a <b>ULONG</b> variable to receive the number of elements in the <i>ppImplList</i> array.


### -param ppImplList [out]

The address of an array of <a href="https://msdn.microsoft.com/0c57aa3f-1d9a-4bb2-b142-bce9c054e658">BCRYPT_PROVIDER_NAME</a> structures to receive the collection of providers that support the specified algorithm. The <i>pImplCount</i> parameter receives the number of elements in this array. This memory must be freed when it is no longer needed by passing this pointer to the <a href="https://msdn.microsoft.com/0ee83ca1-2fe6-4ff2-823e-888b3e66f310">BCryptFreeBuffer</a> function.


### -param dwFlags [in]

A set of flags that modifies the behavior of this function. There are currently no flags defined, so this parameter must be zero.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks




<b>BCryptEnumProviders</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a>.




## -see-also




<a href="https://msdn.microsoft.com/0c57aa3f-1d9a-4bb2-b142-bce9c054e658">BCRYPT_PROVIDER_NAME</a>



<a href="https://msdn.microsoft.com/0ee83ca1-2fe6-4ff2-823e-888b3e66f310">BCryptFreeBuffer</a>
 

 

