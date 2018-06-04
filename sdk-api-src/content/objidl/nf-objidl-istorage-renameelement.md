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

# IStorage::RenameElement


## -description


The <b>RenameElement</b> method renames the specified substorage or stream in this storage object.


## -parameters




### -param pwcsOldName [in]

Pointer to a wide character null-terminated Unicode string that contains the name of the substorage or stream to be changed.

<div class="alert"><b>Note</b>  The <i>pwcsName</i>, created in <a href="https://msdn.microsoft.com/8c74cacf-8d3c-4d57-b1e9-dc5e4f281717">CreateStorage</a> or <a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">CreateStream</a> must not exceed 31 characters in length, not including the string terminator.</div>
<div> </div>

### -param pwcsNewName [in]

Pointer to a wide character null-terminated unicode string that contains the new name for the specified substorage or stream.

<div class="alert"><b>Note</b>  The <i>pwcsName</i>, created in <a href="https://msdn.microsoft.com/8c74cacf-8d3c-4d57-b1e9-dc5e4f281717">CreateStorage</a> or <a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">CreateStream</a> must not exceed 31 characters in length, not including the string terminator.</div>
<div> </div>

## -returns



This method can return one of these values.




## -remarks



<b>IStorage::RenameElement</b> renames the specified substorage or stream in this storage object. An element in a storage object cannot be renamed while it is open. The rename operation is subject to committing the changes if the storage is open in transacted mode.

The <b>IStorage::RenameElement</b> method is not guaranteed to work in low memory with storage objects open in transacted mode. It may work in direct mode.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>
 

 

