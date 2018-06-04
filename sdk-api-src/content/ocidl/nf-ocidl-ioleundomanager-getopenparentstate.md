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

# IOleUndoManager::GetOpenParentState


## -description


Retrieves state information about the innermost open parent undo unit.


## -parameters




### -param pdwState [out]

A pointer to a variable that receives the state information. This information is a value taken from the <a href="https://msdn.microsoft.com/cf711180-e38a-4cff-bd2d-2cfca41b376d">UASFLAGS</a> enumeration.


## -returns



This method returns S_OK if there is an open parent unit and its state was successfully returned or the undo manager is disabled; otherwise, S_FALSE.




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When checking for a normal state, use the UAS_MASK value to mask unused bits in the <i>pdwState</i> parameter to this method for future compatibility. 


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If there is an open parent unit, this method calls <a href="https://msdn.microsoft.com/23eb1768-b68a-4b97-94a4-eeb7b840dda8">IOleParentUndoUnit::GetParentState</a>.

If the undo manager is disabled, it should fill the <i>pdwState</i> parameter with UAS_BLOCKED and return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>



<a href="https://msdn.microsoft.com/cf711180-e38a-4cff-bd2d-2cfca41b376d">UASFLAGS</a>
 

 

