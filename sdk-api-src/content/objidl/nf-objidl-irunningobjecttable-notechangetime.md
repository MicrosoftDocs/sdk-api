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

# IRunningObjectTable::NoteChangeTime


## -description


Records the time that a running object was last modified. The object must have previously been registered with the running object table (ROT). This method stores the time of last change in the ROT.


## -parameters




### -param dwRegister [in]

The identifier of the ROT entry of the changed object. This value was previously returned by <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a>.


### -param pfiletime [in]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the object's last change time.


## -returns



This method can return the standard return values E_INVALIDARG and S_OK.




## -remarks



The time recorded by this method can be retrieved by calling <a href="https://msdn.microsoft.com/fef6f7e5-7d91-4737-98a4-c9779c6c2be5">IRunningObjectTable::GetTimeOfLastChange</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A moniker provider (hands out monikers identifying its objects to make them accessible to others) must call the <b>NoteChangeTime</b> method whenever its objects are modified. It must have previously called <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a> and stored the identifier returned by that method; it uses that identifier when calling <b>NoteChangeTime</b>.



The most common type of moniker provider is a compound-document link source. This includes server applications that support linking to their documents (or portions of a document) and container applications that support linking to embeddings within their documents. Server applications that do not support linking can also use the ROT to cooperate with container applications that support linking to embeddings. 



When an object is first registered in the ROT, the ROT records its last change time as the value returned by calling <a href="https://msdn.microsoft.com/120cc951-6797-4ef6-890b-57ff8d3d23ba">IMoniker::GetTimeOfLastChange</a> on the moniker being registered. 





## -see-also




<a href="https://msdn.microsoft.com/120cc951-6797-4ef6-890b-57ff8d3d23ba">IMoniker::GetTimeOfLastChange</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 

