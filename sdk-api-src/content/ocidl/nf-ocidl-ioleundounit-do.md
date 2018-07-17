---
UID: NF:ocidl.IOleUndoUnit.Do
title: IOleUndoUnit::Do
author: windows-sdk-content
description: Instructs the undo unit to carry out its action. Note that if it contains child undo units, it must call their Do methods as well.
old-location: com\ioleundounit_do.htm
old-project: com
ms.assetid: 5f087779-ef92-41c9-94e6-61d07d5731a7
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Do, Do method [COM], Do method [COM],IOleUndoUnit interface, IOleUndoUnit interface [COM],Do method, IOleUndoUnit.Do, IOleUndoUnit::Do, _ole_ioleundounit_do, com.ioleundounit_do, ocidl/IOleUndoUnit::Do
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleUndoUnit.Do
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleUndoUnit::Do


## -description


Instructs the undo unit to carry out its action. Note that if it contains child undo units, it must call their Do methods as well.


## -parameters




### -param pUndoManager [in]

A pointer to the undo manager. See <a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>.


## -returns



This method returns S_OK on success.




## -remarks



The undo unit is responsible for carrying out its action. Performing its own undo action results in another action that can potentially be reversed. However, if <i>pUndoManager</i> is <b>NULL</b>, the undo unit should perform its undo action but should not attempt to put anything on the redo or undo stack.

If <i>pUndoManager</i> is not <b>NULL</b>, then the unit is required to put a corresponding unit on the redo or undo stack. As a result, this method either moves itself to the redo or undo stack, or it creates a new undo unit and adds it to the appropriate stack. After creating a new undo unit, this undo unit calls <a href="https://msdn.microsoft.com/b494d5b9-5def-4249-8b6d-37b26993cc24">IOleUndoManager::Open</a> or <a href="https://msdn.microsoft.com/3288e0c6-e345-4c4d-a7bf-0c5f45c19732">IOleUndoManager::Add</a>. The undo manager will put the new undo unit on the undo or redo stack depending on its current state.

A parent unit must pass to its children the same undo manager, possibly <b>NULL</b>, that was given to the parent. It is permissible, but not necessary, when <i>pUndoManager</i> is <b>NULL</b> to open a parent unit on the redo or undo stack as long as it is not committed. A blocked parent unit ensures that nothing is added to the stack by child units.

If this undo unit is a parent unit, it should put itself on the redo or undo stack before calling the <b>Do</b> method on its children.

After calling this method, the undo manager must release the undo unit.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
See the <a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a> interface for error handling strategies for undo units. The error handling strategy affects the implementation of this method, particularly for parent units.




## -see-also




<a href="https://msdn.microsoft.com/3288e0c6-e345-4c4d-a7bf-0c5f45c19732">IOleUndoManager::Add</a>



<a href="https://msdn.microsoft.com/b494d5b9-5def-4249-8b6d-37b26993cc24">IOleUndoManager::Open</a>



<a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a>
 

 

