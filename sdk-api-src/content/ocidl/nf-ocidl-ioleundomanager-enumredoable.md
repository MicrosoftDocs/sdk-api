---
UID: NF:ocidl.IOleUndoManager.EnumRedoable
title: IOleUndoManager::EnumRedoable
author: windows-driver-content
description: Creates an enumerator object that the caller can use to iterate through a series of top-level undo units from the redo stack.
old-location: com\ioleundomanager_enumredoable.htm
old-project: com
ms.assetid: f78c7130-34c9-410a-9b9c-222b5e237ad1
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: EnumRedoable, EnumRedoable method [COM], EnumRedoable method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],EnumRedoable method, IOleUndoManager.EnumRedoable, IOleUndoManager::EnumRedoable, _ole_ioleundomanager_enumredoable, com.ioleundomanager_enumredoable, ocidl/IOleUndoManager::EnumRedoable
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IOleUndoManager.EnumRedoable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleUndoManager::EnumRedoable


## -description


Creates an enumerator object that the caller can use to iterate through a series of top-level undo units from the redo stack.


## -parameters




### -param ppEnum [out]

Address of <a href="https://msdn.microsoft.com/f43cbd9d-d91b-4230-816f-693dec7056a4">IEnumOleUndoUnits</a> pointer variable that receives the interface pointer to the enumerator object.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The undo manager is disabled.

</td>
</tr>
</table>
 




## -remarks



A new enumerator object is created each time this method is called. If the series of enumerated items changes over time, the results of enumeration operations can vary from one call to the next.

This method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on the new enumerator object to increment its reference count. The caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on the enumerator object when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/f43cbd9d-d91b-4230-816f-693dec7056a4">IEnumOleUndoUnits</a>



<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>
 

 

