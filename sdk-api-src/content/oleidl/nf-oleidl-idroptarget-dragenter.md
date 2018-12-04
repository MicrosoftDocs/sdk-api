---
UID: NF:oleidl.IDropTarget.DragEnter
title: IDropTarget::DragEnter
author: windows-sdk-content
description: Indicates whether a drop can be accepted, and, if so, the effect of the drop.
old-location: com\idroptarget_dragenter.htm
tech.root: com
ms.assetid: 2e4d7013-910c-4a6e-8eee-818e1f2302ac
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DragEnter, DragEnter method [COM], DragEnter method [COM],IDropTarget interface, IDropTarget interface [COM],DragEnter method, IDropTarget.DragEnter, IDropTarget::DragEnter, _ole_idroptarget_dragenter, com.idroptarget_dragenter, oleidl/IDropTarget::DragEnter
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IDropTarget.DragEnter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDropTarget::DragEnter


## -description


Indicates whether a drop can be accepted, and, if so, the effect of the drop.


## -parameters




### -param pDataObj [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object. This data object contains the data being transferred in the drag-and-drop operation. If the drop occurs, this data object will be incorporated into the target.


### -param grfKeyState [in]

The current state of the keyboard modifier keys on the keyboard. Possible values can be a combination of any of the flags MK_CONTROL, MK_SHIFT, MK_ALT, MK_BUTTON, MK_LBUTTON, MK_MBUTTON, and MK_RBUTTON.


### -param pt [in]

A <a href="https://msdn.microsoft.com/587d36c8-e81c-4256-af25-af2a82727e8d">POINTL</a> structure containing the current cursor coordinates in screen coordinates.


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
The <i>pdwEffect</i> parameter is <b>NULL</b> on input.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



You do not call <b>DragEnter</b> directly; instead the <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> function calls it to determine the effect of a drop the first time the user drags the mouse into the registered window of a drop target.

To implement <b>DragEnter</b>, you must determine whether the target can use the data in the source data object by checking three things:

<ul>
<li>The format and medium specified by the data object</li>
<li>The input value of <i>pdwEffect</i></li>
<li>The state of the modifier keys</li>
</ul>
To check the format and medium, use the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> pointer passed in the <i>pDataObject</i> parameter to call <a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a> so you can enumerate the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures the source data object supports. Then call <a href="https://msdn.microsoft.com/38a1bb4f-7762-4e74-a386-4ae05e59d15f">IDataObject::QueryGetData</a> to determine whether the data object can render the data on the target by examining the formats and medium specified for the data object.

On entry to <b>IDropTarget::DragEnter</b>, the <i>pdwEffect</i> parameter is set to the effects given to the <i>pdwOkEffect</i> parameter of the <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> function. The <b>IDropTarget::DragEnter</b> method must choose one of these effects or disable the drop.

The following modifier keys affect the result of the drop.

<table>
<tr>
<th>Key Combination</th>
<th>User-Visible Feedback</th>
<th>Drop Effect</th>
</tr>
<tr>
<td>CTRL + SHIFT
</td>
<td>=</td>
<td>DROPEFFECT_LINK
</td>
</tr>
<tr>
<td>CTRL
</td>
<td>+
</td>
<td>DROPEFFECT_COPY
</td>
</tr>
<tr>
<td>No keys or SHIFT
</td>
<td>None
</td>
<td>DROPEFFECT_MOVE
</td>
</tr>
</table>
 

On return, the method must write the effect, one of the DROPEFFECT flags, to the <i>pdwEffect</i> parameter. <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> then takes this parameter and writes it to its <i>pdwEffect</i> parameter. You communicate the effect of the drop back to the source through <b>DoDragDrop</b> in the <i>pdwEffect</i> parameter. The <b>DoDragDrop</b> function then calls <a href="https://msdn.microsoft.com/dde37299-ad7c-4f59-af99-e75b72ad9188">IDropSource::GiveFeedback</a> so that the source application can display the appropriate visual feedback to the user through the target window.




## -see-also




<a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">DragEnter</a>



<a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>



<a href="https://msdn.microsoft.com/62ef4fe6-3871-41ef-9542-6fe9f3bed21c">IDropSourceNotify</a>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>



<a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a>
 

 

