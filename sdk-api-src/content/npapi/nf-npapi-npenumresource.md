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

# NPEnumResource function


## -description


Performs an enumeration based on a handle returned by 
<a href="https://msdn.microsoft.com/d8fa7336-3ede-4445-b2e8-1a3efcae22ff">NPOpenEnum</a>.


## -parameters




### -param hEnum [in]

Handle obtained from an 
<a href="https://msdn.microsoft.com/d8fa7336-3ede-4445-b2e8-1a3efcae22ff">NPOpenEnum</a> call.


### -param lpcCount [in, out]

Pointer to the number of entries requested. It may be 0xFFFFFFFF to request as many entries as possible. If the call succeeds, this location will receive the number of entries actually read.


### -param lpBuffer [out]

Pointer to the buffer to receive the enumeration result, which is returned as an array of 
<a href="https://msdn.microsoft.com/c7e22694-2dfd-4a9e-bd40-277611476f97">NETRESOURCE</a> entries. The buffer is valid until the next call using <i>hEnum</i>.


### -param lpBufferSize [in, out]

Pointer to the size, in bytes, of the buffer passed to the function call on entry. If the buffer is too small for even one entry, this should contain, on exit, the number of bytes needed to read one entry. This value is  set only if the return code is WN_MORE_DATA.


## -returns



If the function succeeds, it should return WN_SUCCESS. The caller may continue to call <b>NPEnumResource</b> to continue the enumeration. Otherwise, it should return one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
No more entries. The enumeration was completed successfully. When this occurs, the contents of the return buffer, <i>lpBuffer</i>, are undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to hold even a single entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hEnum</i> is not a valid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present. This condition is checked  before <i>hEnum</i> is tested for validity.

</td>
</tr>
</table>
 




## -remarks



When this function is called, the provider should fill the buffer with the requested number of entries (or the maximum that can fit). The returned 
<a href="https://msdn.microsoft.com/c7e22694-2dfd-4a9e-bd40-277611476f97">NETRESOURCE</a> structures should be located contiguously at the head of the buffer, like an array of such structures. The pointers in these structures must point to locations within the buffer. Therefore, data referenced by these pointers should be located at the end of the buffer, after the array of structures. It is the provider's responsibility to package this information correctly.



