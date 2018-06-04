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

# IFileSystemImage::RollbackToChangePoint


## -description


Reverts the image back to the specified change point.


## -parameters




### -param changePoint [in]

Change point that identifies the target state for rollback.


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
<dt><b>IMAPI_E_TOO_MANY_DIRS</b></dt>
</dl>
</td>
<td width="60%">
This file system image has too many directories for the <i>%1!ls!</i> file system.

Value: 0xC0AAB130

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_ISO9660_LEVELS</b></dt>
</dl>
</td>
<td width="60%">
ISO9660 is limited to 8 levels of directories.

Value: 0xC0AAB131

</td>
</tr>
</table>
 




## -remarks



Typically, an application calls the <a href="https://msdn.microsoft.com/e5d15478-e632-4e76-91e2-ee360dfccf19">IFileSystemImage::get_ChangePoint</a> method and stores the change point value prior to making a change to the file system. If necessary, you can pass the change point value to this method to revert changes since that point in development.

An application can call the <a href="https://msdn.microsoft.com/ae5d659c-5da7-4478-b65f-64cbe227dbc5">IFileSystemImage::LockInChangePoint</a> method to lock the state of  a file system image at any point in its development. After a lock is set, you cannot call this method to revert the file system image to its earlier state.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/ae5d659c-5da7-4478-b65f-64cbe227dbc5">IFileSystemImage::LockInChangePoint</a>



<a href="https://msdn.microsoft.com/e5d15478-e632-4e76-91e2-ee360dfccf19">IFileSystemImage::get_ChangePoint</a>
 

 

