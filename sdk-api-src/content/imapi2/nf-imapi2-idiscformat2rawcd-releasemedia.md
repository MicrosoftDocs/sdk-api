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

# IDiscFormat2RawCD::ReleaseMedia


## -description


Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock.


## -parameters






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
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0602

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0600

</td>
</tr>
</table>
 




## -remarks



This method release the lock set when you called the <a href="https://msdn.microsoft.com/8c393786-0c2d-4244-8ec3-0ac9e47e76c6">IDiscFormat2RawCD::PrepareMedia</a> method. You must call this method after the write operation completes or after calling <a href="https://msdn.microsoft.com/12cd6797-dcb8-496d-a141-9d3a805266e9">IDiscFormat2RawCD::CancelWrite</a> to cancel a writing operation.  




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



IDiscFormat2RawCD::CancelWrite



<a href="https://msdn.microsoft.com/8c393786-0c2d-4244-8ec3-0ac9e47e76c6">IDiscFormat2RawCD::PrepareMedia</a>
 

 

