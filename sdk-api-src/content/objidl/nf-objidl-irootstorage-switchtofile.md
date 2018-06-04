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

# IRootStorage::SwitchToFile


## -description


The 
<b>SwitchToFile</b> method copies the current file associated with the storage object to a new file. The new file is then used for the storage object and any uncommitted changes.


## -parameters




### -param pszFile

A pointer to a null terminated string that specifies the file name for the new file. It cannot be the name of an existing file. If <b>NULL</b>, this method creates a temporary file with a unique name, and you can call 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a> to retrieve the name of the temporary file.


## -returns



This method can return one of these values.




## -remarks



The <b>IRootStorage::SwitchToFile</b> method copies the file associated with the storage object. A COM container calls 
<b>SwitchToFile</b> to perform a full save on a file in a low-memory situation. Typically, this is done only after a normal, full save operation (that is, save to temporary file, delete original file, rename temporary file) has failed with an E_OUTOFMEMORY error.

It is erroneous to call the 
<b>SwitchToFile</b> method if the storage object or anything contained within it has been marshaled to another process. Before calling 
<b>SwitchToFile</b>, the container must call the 
<a href="_com_ipersiststorage_handsoffstorage">IPersistStorage::HandsOffStorage</a> method for any element within the storage object that is loaded or running. The <b>HandsOffStorage</b> method forces the element to release its storage pointers and enter the hands-off storage mode. The container must also release all pointers to streams or storages that are contained in this root storage. After the full save operation is completed, the container returns the contained elements to normal storage mode.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you are implementing your own storage objects, the 
<a href="https://msdn.microsoft.com/cf92c62f-ef65-46b1-8f41-f2b31ff52044">IRootStorage</a> methods (including <a href="_com_iunknown_queryinterface">QueryInterface</a>, <a href="_com_iunknown_addref">AddRef</a>, and <a href="_com_iunknown_release">Release</a>) must not consume additional memory or file handles.




## -see-also




<a href="_com_ipersiststorage_handsoffstorage">IPersistStorage::HandsOffStorage</a>



<a href="_com_ipersiststorage_savecompleted">IPersistStorage::SaveCompleted</a>



<a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>
 

 

