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

# IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize


## -description


Retrieves the maximum non-page-aligned transfer size for the device. 


## -parameters




### -param value [out]

Maximum size, in bytes,  of a non-page-aligned buffer.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>
 




## -remarks



This is the maximum buffer size that a device can accept for a single command. Buffers of this size provide the maximum exchange of data. The buffer does not need to begin on a  physical memory page boundary.




## -see-also




<a href="https://msdn.microsoft.com/37e65b57-ec53-405c-a7bd-34c2df15d5d7">IDiscRecorder2Ex</a>



<a href="https://msdn.microsoft.com/6bf25c61-e87c-4ccf-a989-1c2715709d4a">IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize</a>
 

 

