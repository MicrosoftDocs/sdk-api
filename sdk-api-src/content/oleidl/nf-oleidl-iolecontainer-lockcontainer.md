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

# IOleContainer::LockContainer


## -description


Keeps the container for embedded objects running until explicitly released.


## -parameters




### -param fLock [in]

Indicates whether to lock (<b>TRUE</b>) or unlock (<b>FALSE</b>) a container.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for the operation.

</td>
</tr>
</table>
 




## -remarks



An embedded object calls <b>LockContainer</b> to keep its container running when the object has link clients that require an update. If an end user selects <b>File Close</b> from the container's menu, however, the container ignores all outstanding <b>LockContainer</b> locks and closes the document anyway.




## -see-also




<a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>



<a href="https://msdn.microsoft.com/98549309-8ac8-4391-92ab-8a62269ff579">IOleContainer</a>



<a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a>
 

 

