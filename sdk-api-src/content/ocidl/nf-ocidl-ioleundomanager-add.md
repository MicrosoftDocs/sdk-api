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

# IOleUndoManager::Add


## -description


Adds a simple undo unit to the collection. While a parent undo unit is open, the undo manager adds undo units to it by calling <a href="https://msdn.microsoft.com/86db3308-6f01-47f1-ba28-3ed5e70b7cb9">IOleParentUndoUnit::Add</a>.


## -parameters




### -param pUU [in]

An <a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a> pointer to the undo unit to be added.


## -returns



This method returns S_OK if the specified unit was successfully added, the parent unit was blocked, or the undo manager is disabled.




## -remarks



This method is implemented the same as <a href="https://msdn.microsoft.com/86db3308-6f01-47f1-ba28-3ed5e70b7cb9">IOleParentUndoUnit::Add</a>. The parent undo unit or undo manager must accept any undo unit given to it, unless it is blocked. If it is blocked, it should do nothing but return S_OK.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the undo manager is in the base state, it should put the new unit on the undo stack and discard the entire redo stack. If the undo manager is in the undo state, it should put new units on the redo stack. If the undo manager is in the redo state, it should put units on the undo stack without affecting the redo stack.




## -see-also




<a href="https://msdn.microsoft.com/86db3308-6f01-47f1-ba28-3ed5e70b7cb9">IOleParentUndoUnit::Add</a>



<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>
 

 

