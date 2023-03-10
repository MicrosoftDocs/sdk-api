---
UID: NF:ocidl.IOleUndoManager.GetLastUndoDescription
title: IOleUndoManager::GetLastUndoDescription (ocidl.h)
description: Retrieves the description for the top-level undo unit that is on top of the undo stack.
helpviewer_keywords: ["GetLastUndoDescription","GetLastUndoDescription method [COM]","GetLastUndoDescription method [COM]","IOleUndoManager interface","IOleUndoManager interface [COM]","GetLastUndoDescription method","IOleUndoManager.GetLastUndoDescription","IOleUndoManager::GetLastUndoDescription","_ole_ioleundomanager_getlastundodescription","com.ioleundomanager_getlastundodescription","ocidl/IOleUndoManager::GetLastUndoDescription"]
old-location: com\ioleundomanager_getlastundodescription.htm
tech.root: com
ms.assetid: 65679f9e-2ea8-4462-bdd3-fa12c1904c51
ms.date: 12/05/2018
ms.keywords: GetLastUndoDescription, GetLastUndoDescription method [COM], GetLastUndoDescription method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],GetLastUndoDescription method, IOleUndoManager.GetLastUndoDescription, IOleUndoManager::GetLastUndoDescription, _ole_ioleundomanager_getlastundodescription, com.ioleundomanager_getlastundodescription, ocidl/IOleUndoManager::GetLastUndoDescription
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
 - IOleUndoManager::GetLastUndoDescription
 - ocidl/IOleUndoManager::GetLastUndoDescription
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
 - IOleUndoManager.GetLastUndoDescription
---

# IOleUndoManager::GetLastUndoDescription


## -description

Retrieves the description for the top-level undo unit that is on top of the undo stack.

## -parameters

### -param pBstr [out]

A pointer to a string that contains a description of the top-level undo unit on the undo stack.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The undo stack is empty.

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

This method provides a convenient shortcut for the host application to add a description to its <b>Edit Undo</b> menu item. The <i>pBstr</i> parameter is a string allocated with the standard string allocator. The caller is responsible for freeing this string.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-getlastredodescription">IOleUndoManager::GetLastRedoDescription</a>