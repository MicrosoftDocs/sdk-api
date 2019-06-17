---
UID: NF:ocidl.IOleUndoManager.Add
title: IOleUndoManager::Add (ocidl.h)
author: windows-sdk-content
description: Adds a simple undo unit to the collection. While a parent undo unit is open, the undo manager adds undo units to it by calling IOleParentUndoUnit::Add.
old-location: com\ioleundomanager_add.htm
tech.root: com
ms.assetid: 3288e0c6-e345-4c4d-a7bf-0c5f45c19732
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [COM], Add method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],Add method, IOleUndoManager.Add, IOleUndoManager::Add, _ole_ioleundomanager_add, com.ioleundomanager_add, ocidl/IOleUndoManager::Add
ms.topic: method
f1_keywords: ["ocidl/IOleUndoManager.Add"]
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleUndoManager.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleUndoManager::Add


## -description


Adds a simple undo unit to the collection. While a parent undo unit is open, the undo manager adds undo units to it by calling <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-add">IOleParentUndoUnit::Add</a>.


## -parameters




### -param pUU [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a> pointer to the undo unit to be added.


## -returns



This method returns S_OK if the specified unit was successfully added, the parent unit was blocked, or the undo manager is disabled.




## -remarks



This method is implemented the same as <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-add">IOleParentUndoUnit::Add</a>. The parent undo unit or undo manager must accept any undo unit given to it, unless it is blocked. If it is blocked, it should do nothing but return S_OK.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the undo manager is in the base state, it should put the new unit on the undo stack and discard the entire redo stack. If the undo manager is in the undo state, it should put new units on the redo stack. If the undo manager is in the redo state, it should put units on the undo stack without affecting the redo stack.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-add">IOleParentUndoUnit::Add</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>
 

 

