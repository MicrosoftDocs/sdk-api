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

# IFileSystemImage::LockInChangePoint


## -description


Locks the file system information at the current change-point level.


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
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal error occurred: <i>%1!ls!</i>.

</td>
</tr>
</table>
 




## -remarks



Once the change point is locked, rollback to earlier change points is not permitted.

Locking the change point does not change the <a href="https://msdn.microsoft.com/e5d15478-e632-4e76-91e2-ee360dfccf19">IFileSystemImage::get_ChangePoint</a> property.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/852b88ed-6af7-4fe6-bf5f-831d55423130">IFileSystemImage::RollbackToChangePoint</a>



<a href="https://msdn.microsoft.com/e5d15478-e632-4e76-91e2-ee360dfccf19">IFileSystemImage::get_ChangePoint</a>
 

 

