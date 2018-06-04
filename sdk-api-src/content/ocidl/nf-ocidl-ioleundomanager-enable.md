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

If the undo manager is disabled, each method in <a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a> must behave as specified. See each method for details.




## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>
 

 

