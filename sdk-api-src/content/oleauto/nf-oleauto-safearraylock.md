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

# SafeArrayLock function


## -description


Increments the lock count of an array, and places a pointer to the array data in pvData of the array descriptor.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The array could not be locked.

</td>
</tr>
</table>
 




## -remarks



The pointer in the array descriptor is valid until the <a href="https://msdn.microsoft.com/654995ab-1959-44dc-9e26-11c34e489c14">SafeArrayUnlock</a> function is called. Calls to <b>SafeArrayLock</b> can be nested, in which case an equal number of calls to <b>SafeArrayUnlock</b> are required.

An array cannot be deleted while it is locked.


#### Thread Safety

All public static (Shared in Visual Basic) members of the <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY data type</a> are thread safe. Instance members are not guaranteed to be thread safe.

For example, consider an application that uses the SafeArrayLock and <a href="https://msdn.microsoft.com/654995ab-1959-44dc-9e26-11c34e489c14">SafeArrayUnlock</a> functions. If these functions are called concurrently from different threads on the same <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY data type</a> instance, an inconsistent lock count may be created. This will eventually cause the <b>SafeArrayUnlock</b> function to return E_UNEXPECTED. You can prevent this by providing your own synchronization code.



