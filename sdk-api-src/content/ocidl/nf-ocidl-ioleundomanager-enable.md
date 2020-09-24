---
UID: NF:ocidl.IOleUndoManager.Enable
title: IOleUndoManager::Enable (ocidl.h)
description: Enables or disables the undo manager.
helpviewer_keywords: ["Enable","Enable method [COM]","Enable method [COM]","IOleUndoManager interface","IOleUndoManager interface [COM]","Enable method","IOleUndoManager.Enable","IOleUndoManager::Enable","_ole_ioleundomanager_enable","com.ioleundomanager_enable","ocidl/IOleUndoManager::Enable"]
old-location: com\ioleundomanager_enable.htm
tech.root: com
ms.assetid: d4d8582e-a9d1-48df-87ef-e378f3a81fa2
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [COM], Enable method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],Enable method, IOleUndoManager.Enable, IOleUndoManager::Enable, _ole_ioleundomanager_enable, com.ioleundomanager_enable, ocidl/IOleUndoManager::Enable
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
 - IOleUndoManager::Enable
 - ocidl/IOleUndoManager::Enable
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
 - IOleUndoManager.Enable
---

# IOleUndoManager::Enable


## -description

Enables or disables the undo manager.

## -parameters

### -param fEnable [in]

Indicates whether to enable or disable the undo manager. If <b>TRUE</b>, the undo manager should be enabled. If <b>FALSE</b>, the undo manager should be disabled.

## -returns

This method returns S_OK if the undo manager was successfully enabled or disabled. Other possible return values include the following.

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
There is an open undo unit on the stack or the undo manager is currently performing an undo or a redo.

</td>
</tr>
</table>

## -remarks

The undo manager should clear both stacks when making the transition from enabled to disabled.

If the undo manager is disabled, each method in <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a> must behave as specified. See each method for details.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>