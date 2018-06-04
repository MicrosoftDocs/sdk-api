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

# IEnumEnhancedStorageACT::GetMatchingACT


## -description


Returns the Addressable Command Target (ACT) associated with the volume specified via the string supplied by the client.


## -parameters




### -param szVolume [in]

A string that specifies the volume for which a matching ACT is searched for.


### -param ppIEnhancedStorageACT [out]

Pointer to an <b>IEnhancedStorageACT</b> interface pointer that represents the matching ACT. If no matching ACT is found the error <b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b> is returned.


## -returns



This method can return one of these values.

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
A matching ACT was successfully found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>szVolume</i> or <i>ppIEnhancedStorageACT</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A matching ACT wasn't found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
Enhanced storage is not supported on the device containing <i>szVolume</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_FUNCTION)</b></dt>
</dl>
</td>
<td width="60%">
Enhanced storage is not supported on the device containing <i>szVolume</i>.

</td>
</tr>
</table>
 




## -remarks



This method can also be utilized by the client to determine if the specified volume resides on, and is represented by an IEEE 1667 ACT.




## -see-also




<a href="https://msdn.microsoft.com/807834cc-0f52-43f6-a3b3-06591ba68c15">IEnumEnhancedStorageACT</a>
 

 

