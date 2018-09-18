---
UID: NF:ocidl.IOleUndoManager.GetLastRedoDescription
title: IOleUndoManager::GetLastRedoDescription
author: windows-sdk-content
description: Retrieves the description for the top-level undo unit that is on top of the redo stack.
old-location: com\ioleundomanager_getlastredodescription.htm
tech.root: com
ms.assetid: b3d514cf-1d1f-4b5b-89f6-d0e03aa794cc
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetLastRedoDescription, GetLastRedoDescription method [COM], GetLastRedoDescription method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],GetLastRedoDescription method, IOleUndoManager.GetLastRedoDescription, IOleUndoManager::GetLastRedoDescription, _ole_ioleundomanager_getlastredodescription, com.ioleundomanager_getlastredodescription, ocidl/IOleUndoManager::GetLastRedoDescription
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
 - IOleUndoManager.GetLastRedoDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUndoManager::GetLastRedoDescription


## -description


Retrieves the description for the top-level undo unit that is on top of the redo stack.


## -parameters




### -param pBstr [out]

A pointer to a string that contains a description of the top-level undo unit on the redo stack.


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



This method provides a convenient shortcut for the host application to add a description to its <b>Edit Redo</b> menu item. The <i>pBstr</i> parameter is a string allocated with the standard string allocator. The caller is responsible for freeing this string.




## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>



<a href="https://msdn.microsoft.com/65679f9e-2ea8-4462-bdd3-fa12c1904c51">IOleUndoManager::GetLastUndoDescription</a>
 

 

