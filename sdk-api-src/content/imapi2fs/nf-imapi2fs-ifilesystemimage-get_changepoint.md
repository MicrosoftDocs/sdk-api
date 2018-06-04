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

# IFileSystemImage::get_ChangePoint


## -description


Retrieves the change point identifier.


## -parameters




### -param pVal [out]

Change point identifier. The identifier is a count of the changes to the file system image since its inception.


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
</table>
 




## -remarks



An application can store the value of this property prior to making a change to the file system, then at a later point pass the value to the <a href="https://msdn.microsoft.com/852b88ed-6af7-4fe6-bf5f-831d55423130">IFileSystemImage::RollbackToChangePoint</a> method to revert changes since that point in development.

An application can call the <a href="https://msdn.microsoft.com/ae5d659c-5da7-4478-b65f-64cbe227dbc5">IFileSystemImage::LockInChangePoint</a> method to lock the state of  a file system image at any point in its development. Once a lock is set, you cannot call <a href="https://msdn.microsoft.com/852b88ed-6af7-4fe6-bf5f-831d55423130">RollbackToChangePoint</a> to revert the file system image to its earlier state.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/ae5d659c-5da7-4478-b65f-64cbe227dbc5">IFileSystemImage::LockInChangePoint</a>



<a href="https://msdn.microsoft.com/852b88ed-6af7-4fe6-bf5f-831d55423130">IFileSystemImage::RollbackToChangePoint</a>
 

 

