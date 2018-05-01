---
UID: NF:ocidl.IOleUndoManager.Enable
title: IOleUndoManager::Enable method
author: windows-driver-content
description: Enables or disables the undo manager.
old-location: com\ioleundomanager_enable.htm
old-project: com
ms.assetid: d4d8582e-a9d1-48df-87ef-e378f3a81fa2
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: Enable method [COM], Enable method [COM], IOleUndoManager interface, Enable,IOleUndoManager.Enable, IOleUndoManager, IOleUndoManager interface [COM], Enable method, IOleUndoManager::Enable, _ole_ioleundomanager_enable, com.ioleundomanager_enable, ocidl/IOleUndoManager::Enable
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
-	IOleUndoManager.Enable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleUndoManager::Enable method


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

If the undo manager is disabled, each method in <a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a> must behave as specified. See each method for details.




## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>
 

 

