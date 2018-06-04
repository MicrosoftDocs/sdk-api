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

# ICreateDeviceAccessAsync::GetResult


## -description


Retrieves an <a href="https://msdn.microsoft.com/d285e04e-04d0-4c2a-b9f0-72eebebf4f4b">IDeviceIoControl</a> object that's bound to the device interface that's specified in a call to the <a href="https://msdn.microsoft.com/082d6297-20ac-4557-8205-0451482a5758">CreateDeviceAccessInstance</a> function.


## -parameters




### -param riid [in]

An interface identifier that indicates what type of device access interface the caller wants to retrieve. The only valid value for this identifier is IID_IDeviceIoControl.


### -param deviceAccess [out]

If the binding was successful, contains an interface of the type that was supplied to the initial call to <a href="https://msdn.microsoft.com/082d6297-20ac-4557-8205-0451482a5758">CreateDeviceAccessInstance</a>.


## -returns



This method supports standard return values, in addition to these:

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
The binding was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation wasn't in a valid state. The bind operation was either still in progress or not yet started.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ebc8d694-c933-4d98-95f5-67b0dd733d4d">ICreateDeviceAccessAsync</a>
 

 

