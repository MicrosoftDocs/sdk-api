---
UID: NF:oleidl.IDropTarget.DragLeave
title: IDropTarget::DragLeave
author: windows-sdk-content
description: Removes target feedback and releases the data object.
old-location: com\idroptarget_dragleave.htm
old-project: com
ms.assetid: 2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DragLeave, DragLeave method [COM], DragLeave method [COM],IDropTarget interface, IDropTarget interface [COM],DragLeave method, IDropTarget.DragLeave, IDropTarget::DragLeave, _ole_idroptarget_dragleave, com.idroptarget_dragleave, oleidl/IDropTarget::DragLeave
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IDropTarget.DragLeave
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IDropTarget::DragLeave


## -description


Removes target feedback and releases the data object.


## -parameters






## -returns



This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



You do not call this method directly. The <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> function calls this method in either of the following cases:

<ul>
<li>When the user drags the cursor out of a given target window.</li>
<li>When the user cancels the current drag-and-drop operation.</li>
</ul>
To implement <b>IDropTarget::DragLeave</b>, you must remove any target feedback that is currently displayed. You must also release any references you hold to the data transfer object.




## -see-also




<a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a>



<a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>



<a href="https://msdn.microsoft.com/62ef4fe6-3871-41ef-9542-6fe9f3bed21c">IDropSourceNotify</a>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>



<a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a>
 

 

