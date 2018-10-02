---
UID: NF:ocidl.IOleUndoManager.RedoTo
title: IOleUndoManager::RedoTo
author: windows-sdk-content
description: Instructs the undo manager to invoke undo actions back through the redo stack, down to and including the specified undo unit.
old-location: com\ioleundomanager_redoto.htm
tech.root: com
ms.assetid: 1d5d0cb6-2c1b-49c8-8923-59845fa6231c
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IOleUndoManager interface [COM],RedoTo method, IOleUndoManager.RedoTo, IOleUndoManager::RedoTo, RedoTo, RedoTo method [COM], RedoTo method [COM],IOleUndoManager interface, _ole_ioleundomanager_redoto, com.ioleundomanager_redoto, ocidl/IOleUndoManager::RedoTo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOleUndoManager.RedoTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUndoManager::RedoTo


## -description


Instructs the undo manager to invoke undo actions back through the redo stack, down to and including the specified undo unit.


## -parameters




### -param pUU [in]

An <a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a> pointer to the top level unit to redo. If this parameter is <b>NULL</b>, the most recently added top level unit is used.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified undo unit is not on the redo stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Both the undo attempt and the rollback attempt failed. The undo manager should never propagate the E_ABORT obtained from a contained undo unit. Instead, it should map any E_ABORT values returned from other undo units to E_FAIL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The undo manager is disabled.

</td>
</tr>
</table>
 




## -remarks



This method calls the <a href="https://msdn.microsoft.com/5f087779-ef92-41c9-94e6-61d07d5731a7">IOleUndoUnit::Do</a> method on each top-level undo unit. Then, it releases that undo unit.

Note that the specified undo unit must be a top-level unit, typically retrieved through <a href="https://msdn.microsoft.com/f78c7130-34c9-410a-9b9c-222b5e237ad1">IOleUndoManager::EnumRedoable</a>.

In case an error is returned from the undo unit, the undo manager needs to attempt to rollback the state of the document to recover from the error by performing actions on the undo stack.

No matter what the success of the rollback, the undo manager should always clear both stacks before returning the error.

If the undo manager has called the <a href="https://msdn.microsoft.com/5f087779-ef92-41c9-94e6-61d07d5731a7">IOleUndoUnit::Do</a> method on more than one top-level unit, it should only rollback the unit that returned the error. The top-level units that succeeded should not be rolled back.

The undo manager must also keep track of whether units were added to the opposite stack so it won't attempt rollback if nothing was added. See the <a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a> interface for detailed description of error handling.




## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>



<a href="https://msdn.microsoft.com/f78c7130-34c9-410a-9b9c-222b5e237ad1">IOleUndoManager::EnumRedoable</a>



<a href="https://msdn.microsoft.com/49c98126-4b99-449e-b08c-f21f98c7c56a">IOleUndoManager::UndoTo</a>



<a href="https://msdn.microsoft.com/5f087779-ef92-41c9-94e6-61d07d5731a7">IOleUndoUnit::Do</a>
 

 

