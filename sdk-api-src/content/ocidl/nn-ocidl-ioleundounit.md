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

# IOleUndoUnit interface


## -description


Serves as the main interface on an undo unit. An undo unit encapsulates the information necessary to undo or redo a single action.

When an object's state changes and it needs to create an undo unit, it first needs to know what parent units are open. It calls the <a href="https://msdn.microsoft.com/32a4e08a-409b-4f0e-8374-1cdf3b558928">IOleUndoManager::GetOpenParentState</a> method to determine this. If the call returns S_FALSE, then there is no enabling parent. If the call returns S_OK but the UAS_NOPARENTENABLE flag is set, then the open parent is a disabling parent. In either of these cases, the object calls <a href="https://msdn.microsoft.com/eb742d04-63cb-4505-bc91-8d87267a3a4a">IOleUndoManager::DiscardFrom</a>(NULL) on the undo manager and skips creating the undo unit.

If the method returns S_OK, but the UAS_BLOCKED flag is set, then the open parent is a blocking parent. The object does not need to create an undo unit, since it would be immediately discarded. If the return value is S_OK and neither of the bit flags are set, then the object creates the undo unit and calls <a href="https://msdn.microsoft.com/3288e0c6-e345-4c4d-a7bf-0c5f45c19732">IOleUndoManager::Add</a> on the undo manager.

The object should retain a pointer to the undo manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUndoUnit</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleUndoUnit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUndoUnit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f087779-ef92-41c9-94e6-61d07d5731a7">Do</a>
</td>
<td align="left" width="63%">
Instructs the undo unit to carry out its action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the undo unit that can be used in the undo or redo user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f0c719e-75cd-48dd-8bd8-78eb63cc141a">GetUnitType</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID and a type identifier for the undo unit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79bbdb6c-cae3-4f9a-b335-565aacec6d3e">OnNextAdd</a>
</td>
<td align="left" width="63%">
Notifies the last undo unit in the collection that a new unit has been added.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>



<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>
 

 

