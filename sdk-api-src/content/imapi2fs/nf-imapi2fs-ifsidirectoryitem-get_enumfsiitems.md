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

# IFsiDirectoryItem::get_EnumFsiItems


## -description


Retrieves a list of child items contained within the directory in the file system image.


## -parameters




### -param NewEnum [out]

An <a href="https://msdn.microsoft.com/f3186af1-4056-4cb5-aac4-5253ee6dbc01">IEnumFsiItems</a> interface that contains a collection of the child directory and file items contained within the directory.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -remarks



This property returns the same results as the <a href="https://msdn.microsoft.com/08ffc4dd-7001-4a89-a58e-a12e21600172">IFsiDirectoryItem::get__NewEnum</a> property and is meant for use by C/C++ applications.




## -see-also




<a href="https://msdn.microsoft.com/f3186af1-4056-4cb5-aac4-5253ee6dbc01">IEnumFsiItems</a>



<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>



<a href="https://msdn.microsoft.com/08ffc4dd-7001-4a89-a58e-a12e21600172">IFsiDirectoryItem::get__NewEnum</a>
 

 

