---
UID: NF:ocidl.IOleUndoManager.EnumUndoable
title: IOleUndoManager::EnumUndoable (ocidl.h)
description: Creates an enumerator object that the caller can use to iterate through a series of top-level undo units from the undo stack.
helpviewer_keywords: ["EnumUndoable","EnumUndoable method [COM]","EnumUndoable method [COM]","IOleUndoManager interface","IOleUndoManager interface [COM]","EnumUndoable method","IOleUndoManager.EnumUndoable","IOleUndoManager::EnumUndoable","_ole_ioleundomanager_enumundoable","com.ioleundomanager_enumundoable","ocidl/IOleUndoManager::EnumUndoable"]
old-location: com\ioleundomanager_enumundoable.htm
tech.root: com
ms.assetid: 7199910b-3ea3-4b4e-89df-c1188195941c
ms.date: 12/05/2018
ms.keywords: EnumUndoable, EnumUndoable method [COM], EnumUndoable method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],EnumUndoable method, IOleUndoManager.EnumUndoable, IOleUndoManager::EnumUndoable, _ole_ioleundomanager_enumundoable, com.ioleundomanager_enumundoable, ocidl/IOleUndoManager::EnumUndoable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleUndoManager::EnumUndoable
 - ocidl/IOleUndoManager::EnumUndoable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleUndoManager.EnumUndoable
---

# IOleUndoManager::EnumUndoable


## -description

Creates an enumerator object that the caller can use to iterate through a series of top-level undo units from the undo stack.

## -parameters

### -param ppEnum [out]

Address of <a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a> pointer variable that receives the interface pointer to the enumerator object.

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

This method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the new enumerator object to increment its reference count. The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the enumerator object when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>