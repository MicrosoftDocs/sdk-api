---
UID: NF:ole2.DoDragDrop
title: DoDragDrop function
author: windows-driver-content
description: Carries out an OLE drag and drop operation.
old-location: com\dodragdrop.htm
old-project: com
ms.assetid: 095172ac-9e08-4797-b9da-41a4e5a61315
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: DoDragDrop, DoDragDrop function [COM], _ole_DoDragDrop, com.dodragdrop, ole2/DoDragDrop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	ext-ms-win-com-ole32-l1-1-3.dll
-	Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
-	DoDragDrop
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# DoDragDrop function


## -description


Carries out an OLE drag and drop operation.


<div class="alert"><b>Note</b>  You must call <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before calling this function.</div><div> </div>

## -parameters




### -param pDataObj [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on a data object that contains the data being dragged.


### -param pDropSource [in]

Pointer to an implementation of the <a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a> interface, which is used to communicate with the source during the drag operation.


### -param dwOKEffects [in]

Effects the source allows in the OLE drag-and-drop operation. Most significant is whether it permits a move. The <i>dwOKEffect</i> and <i>pdwEffect</i> parameters obtain values from the <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a> enumeration. For a list of values, see <b>DROPEFFECT</b>.


### -param pdwEffect [out]

 Pointer to a value that indicates how the OLE drag-and-drop operation affected the source data. The <i>pdwEffect</i> parameter is set only if the operation is not canceled.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_DROP</b></dt>
</dl>
</td>
<td width="60%">
The OLE drag-and-drop operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The OLE drag-and-drop operation was canceled. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSPEC</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



If you are developing an application that can act as a data source for an OLE drag-and-drop operation, you must call <b>DoDragDrop</b> when you detect that the user has started an OLE drag-and-drop operation.



The <b>DoDragDrop</b> function enters a loop in which it calls various methods in the <a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a> and <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interfaces. (For a successful drag-and-drop operation, the application acting as the data source must also implement <b>IDropSource</b>, while the target application must implement <b>IDropTarget</b>.) 

<ol>
<li>
The <b>DoDragDrop</b> function determines the window under the current cursor location. It then checks to see if this window is a valid drop target.


</li>
<li>
 If the window is a valid drop target, <b>DoDragDrop</b> calls <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a>. This method supplies an effect code indicating what would happen if the drop actually occurred. For a list of valid drop effects, see the <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a> enumeration.

</li>
<li>
<b>DoDragDrop</b> calls <a href="https://msdn.microsoft.com/dde37299-ad7c-4f59-af99-e75b72ad9188">IDropSource::GiveFeedback</a> with the effect code so that the drop source interface can provide appropriate visual feedback to the user. The <i>pDropSource</i> pointer passed into <b>DoDragDrop</b> specifies the appropriate <a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a> interface.


</li>
<li>
<b>DoDragDrop</b> tracks mouse cursor movements and changes in the keyboard or mouse button state.

<ul>
<li>
If the user moves out of a window, <b>DoDragDrop</b> calls <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a>.


</li>
<li>
If the mouse enters another window, <b>DoDragDrop</b> determines if that window is a valid drop target and then calls <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> for that window.

</li>
<li>
If the mouse moves but stays within the same window, <b>DoDragDrop</b> calls <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a>.


</li>
</ul>
</li>
<li>
If there is a change in the keyboard or mouse button state, <b>DoDragDrop</b> calls <a href="https://msdn.microsoft.com/96ea44fc-5046-4e31-abfc-659d8ef3ca8f">IDropSource::QueryContinueDrag</a> and determines whether to continue the drag, to drop the data, or to cancel the operation based on the return value. 


<ul>
<li>
If the return value is S_OK, <b>DoDragDrop</b> first calls <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> to continue the operation. This method returns a new effect value and <b>DoDragDrop</b> then calls <a href="https://msdn.microsoft.com/dde37299-ad7c-4f59-af99-e75b72ad9188">IDropSource::GiveFeedback</a> with the new effect so appropriate visual feedback can be set. For a list of valid drop effects, see the <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a> enumeration. <b>IDropTarget::DragOver</b> and <b>IDropSource::GiveFeedback</b> are paired so that as the mouse moves across the drop target, the user is given the most up-to-date feedback on the mouse's position.

</li>
<li>
If the return value is DRAGDROP_S_DROP, <b>DoDragDrop</b> calls <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a>. The <b>DoDragDrop</b> function returns the last effect code to the source, so the source application can perform the appropriate operation on the source data, for example, cut the data if the operation was a move.


</li>
<li>
If the return value is DRAGDROP_S_CANCEL, the <b>DoDragDrop</b> function calls <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a>.


</li>
</ul>
</li>
</ol>
<b>DoDragDrop</b> does not support invoking drag and drop support when you handle touch or pen input.

To support touch or pen input, do not call <b>DoDragDrop</b> from your touch handler. Instead, call <b>DoDragDrop</b> from your handler for those mouse messages that the system synthesizes upon touch input.

The application can identify synthesized messages by calling the <a href="https://msdn.microsoft.com/c2b978b4-165b-44a0-8091-580e82f7e310">GetMessageExtraInfo</a> function. For more information about using <b>GetMessageExtraInfo</b> to distinguish between mouse input and Windows Touch input,  see <a href="https://msdn.microsoft.com/dfdc5a97-aa0a-4011-8f61-6e405e28b6f8">Troubleshooting Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>
 

 

