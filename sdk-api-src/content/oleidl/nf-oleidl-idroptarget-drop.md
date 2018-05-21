---
UID: NF:oleidl.IDropTarget.Drop
title: IDropTarget::Drop
author: windows-driver-content
description: Incorporates the source data into the target window, removes target feedback, and releases the data object.
old-location: com\idroptarget_drop.htm
old-project: com
ms.assetid: 7ea6d815-bf8f-47d5-99d3-f9a55bafee2e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: Drop, Drop method [COM], Drop method [COM],IDropTarget interface, IDropTarget interface [COM],Drop method, IDropTarget.Drop, IDropTarget::Drop, _ole_idroptarget_drop, com.idroptarget_drop, oleidl/IDropTarget::Drop
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IDropTarget.Drop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDropTarget::Drop


## -description


Incorporates the source data into the target window, removes target feedback, and releases the data object.


## -parameters




### -param pDataObj [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object being transferred in the drag-and-drop operation.


### -param grfKeyState [in]

The current state of the keyboard modifier keys on the keyboard. Possible values can be a combination of any of the flags MK_CONTROL, MK_SHIFT, MK_ALT, MK_BUTTON, MK_LBUTTON, MK_MBUTTON, and MK_RBUTTON.


### -param pt [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure containing the current cursor coordinates in screen coordinates.


### -param pdwEffect [in, out]

On input, pointer to the value of the <i>pdwEffect</i> parameter of the <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> function. On return, must contain one of the <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a> flags, which indicates what the result of the drop operation would be.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwEffect</i> parameter is not valid.

</td>
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



You do not call this method directly. The <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> function calls this method when the user completes the drag-and-drop operation.

In implementing <b>Drop</b>, you must incorporate the data object into the target. Use the formats available in <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, available through <i>pDataObj</i>, along with the current state of the modifier keys to determine how the data is to be incorporated, such as linking or embedding.

In addition to incorporating the data, you must also clean up as you do in the <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> method:

<ul>
<li>Remove any target feedback that is currently displayed.</li>
<li>Release any references to the data object.</li>
</ul>
You also pass the effect of this operation back to the source application through <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a>, so the source application can clean up after the drag-and-drop operation is complete:

<ul>
<li>Remove any source feedback that is being displayed.</li>
<li>Make any necessary changes to the data, such as removing the data if the operation was a move.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a>



<a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>



<a href="https://msdn.microsoft.com/62ef4fe6-3871-41ef-9542-6fe9f3bed21c">IDropSourceNotify</a>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>



<a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a>
 

 

