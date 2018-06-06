---
UID: NF:ocidl.IOleParentUndoUnit.GetParentState
title: IOleParentUndoUnit::GetParentState
author: windows-sdk-content
description: Retrieves state information about the innermost open parent undo unit.
old-location: com\ioleparentundounit_getparentstate.htm
old-project: com
ms.assetid: 23eb1768-b68a-4b97-94a4-eeb7b840dda8
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetParentState, GetParentState method [COM], GetParentState method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],GetParentState method, IOleParentUndoUnit.GetParentState, IOleParentUndoUnit::GetParentState, _ole_ioleparentundounit_getparentstate, com.ioleparentundounit_getparentstate, ocidl/IOleParentUndoUnit::GetParentState
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
 - IOleParentUndoUnit.GetParentState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleParentUndoUnit::GetParentState


## -description


Retrieves state information about the innermost open parent undo unit.


## -parameters




### -param pdwState [out]

A pointer to the state information. This information is a value taken from the <a href="https://msdn.microsoft.com/cf711180-e38a-4cff-bd2d-2cfca41b376d">UASFLAGS</a> enumeration.


## -returns



This method returns S_OK on success.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the unit has an open child, it should delegate this method to that child. If not, it should fill in <i>pdwState</i> values appropriately and return. Note that a parent unit must never be blocked while it has an open child. If this happened it could prevent the child unit from being closed, which would cause serious problems.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When checking for a normal state, use the UAS_MASK value to mask unused bits in the <i>pdwState</i> parameter to this method for future compatibility.




## -see-also




<a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>
 

 

