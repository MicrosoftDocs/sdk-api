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

# IOleUndoManager::DiscardFrom


## -description


Instructs the undo manager to discard the specified undo unit and all undo units below it on the undo or redo stack.


## -parameters




### -param pUU [in]

An <a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a> pointer to the undo unit to be discarded. This parameter can be <b>NULL</b> to discard the entire undo or redo stack. If the parameter is not <b>NULL</b> then the stack will not be discarded.


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
The specified undo unit was not found in the stacks.

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



The undo manager first searches the undo stack for the given unit, and if not found there searches the redo stack. After it has been found, the given unit and all below it on the same stack are discarded. The undo unit may be a child of a parent unit contained by the undo manager, as determined by calling <a href="https://msdn.microsoft.com/096e6cc4-7843-49fa-b1d7-bce034d4b7ce">IOleParentUndoUnit::FindUnit</a>. If it is a child unit, then the root unit containing the given unit and all units below it on the appropriate stack are discarded.

If there is an open parent unit and the <b>DiscardFrom</b> method is called and the <i>pUU</i> parameter is <b>NULL</b>, the undo manager should immediately release and discard the open parent unit without calling the <a href="https://msdn.microsoft.com/4546f270-5cef-42a3-b07a-f0a491e78849">IOleUndoManager::Close</a> first. When the object that opened the parent unit attempts to close it, <b>IOleUndoManager::Close</b> will return S_FALSE. If a parent unit is open, throw it away and discard the stack. If the parent unit is not open, just throw the stack away. If the <i>pUU</i> parameter is not <b>NULL</b>, then any open parent units should be left open.




## -see-also




<a href="https://msdn.microsoft.com/096e6cc4-7843-49fa-b1d7-bce034d4b7ce">IOleParentUndoUnit::FindUnit</a>



<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>



<a href="https://msdn.microsoft.com/4546f270-5cef-42a3-b07a-f0a491e78849">IOleUndoManager::Close</a>
 

 

