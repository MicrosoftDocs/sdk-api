---
UID: NF:objidl.IStorage.RenameElement
title: IStorage::RenameElement
author: windows-sdk-content
description: The RenameElement method renames the specified substorage or stream in this storage object.
old-location: stg\istorage_renameelement.htm
old-project: stg
ms.assetid: 9d88b2e0-8b68-4607-8f96-5e36e831c283
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IStorage interface [Structured Storage],RenameElement method, IStorage.RenameElement, IStorage::RenameElement, RenameElement, RenameElement method [Structured Storage], RenameElement method [Structured Storage],IStorage interface, _stg_istorage_renameelement, objidl/IStorage::RenameElement, stg.istorage_renameelement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.RenameElement
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
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
 

 

