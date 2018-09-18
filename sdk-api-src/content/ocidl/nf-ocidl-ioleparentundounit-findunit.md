---
UID: NF:ocidl.IOleParentUndoUnit.FindUnit
title: IOleParentUndoUnit::FindUnit
author: windows-sdk-content
description: Indicates whether the specified unit is a child of this undo unit or one of its children, that is if the specified unit is part of the hierarchy in this parent unit.
old-location: com\ioleparentundounit_findunit.htm
tech.root: com
ms.assetid: 096e6cc4-7843-49fa-b1d7-bce034d4b7ce
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: FindUnit, FindUnit method [COM], FindUnit method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],FindUnit method, IOleParentUndoUnit.FindUnit, IOleParentUndoUnit::FindUnit, _ole_ioleparentundounit_findunit, com.ioleparentundounit_findunit, ocidl/IOleParentUndoUnit::FindUnit
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
 - IOleParentUndoUnit.FindUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleParentUndoUnit::FindUnit


## -description


Indicates whether the specified unit is a child of this undo unit or one of its children, that is if the specified unit is part of the hierarchy in this parent unit.


## -parameters




### -param pUU [in]

 An <a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a> pointer to the undo unit to be found.


## -returns



This method returns S_OK if the specified undo unit is in the hierarchy subordinate to this parent; otherwise, S_FALSE.




## -remarks



This is typically called by the undo manager in its implementation of its <a href="https://msdn.microsoft.com/eb742d04-63cb-4505-bc91-8d87267a3a4a">IOleUndoManager::DiscardFrom</a> method in the rare event that the unit being discarded is not a top-level unit. The parent unit should look in its own list first, then delegate to each child that is also a parent unit, as determined by doing a <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> for <a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>.




## -see-also




<a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>



<a href="https://msdn.microsoft.com/eb742d04-63cb-4505-bc91-8d87267a3a4a">IOleUndoManager::DiscardFrom</a>
 

 

