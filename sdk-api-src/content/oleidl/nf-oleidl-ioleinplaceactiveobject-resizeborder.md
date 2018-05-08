---
UID: NF:oleidl.IOleInPlaceActiveObject.ResizeBorder
title: IOleInPlaceActiveObject::ResizeBorder
author: windows-driver-content
description: Alerts the object that it needs to resize its border space.
old-location: com\ioleinplaceactiveobject_resizeborder.htm
old-project: com
ms.assetid: 240d2ae5-abce-4bea-969e-f47780908bbb
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IOleInPlaceActiveObject interface [COM],ResizeBorder method, IOleInPlaceActiveObject.ResizeBorder, IOleInPlaceActiveObject::ResizeBorder, ResizeBorder, ResizeBorder method [COM], ResizeBorder method [COM],IOleInPlaceActiveObject interface, _ole_ioleinplaceactiveobject_resizeborder, com.ioleinplaceactiveobject_resizeborder, oleidl/IOleInPlaceActiveObject::ResizeBorder
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
-	IOleInPlaceActiveObject.ResizeBorder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleInPlaceActiveObject::ResizeBorder


## -description


Alerts the object that it needs to resize its border space.


## -parameters




### -param prcBorder [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the new outer rectangle within which the object can request border space for its tools.


### -param pUIWindow [in]

A pointer to an <a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a> interface pointer for the frame or document window object whose border has changed.


### -param fFrameWindow [in]

This parameter is <b>TRUE</b> if the frame window object is calling <b>IOleInPlaceActiveObject::ResizeBorder</b>; otherwise, it is <b>FALSE</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter values are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>IOleInPlaceActiveObject::ResizeBorder</b> is called by the top-level container's document or frame window object when the border space allocated to the object should change. Because the active in-place object is not informed about which window has changed (the frame- or document-level window), <b>IOleInPlaceActiveObject::ResizeBorder</b> must be passed the pointer to the window's <a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a> interface.


<h3><a id="Notes_to_Implemeters"></a><a id="notes_to_implemeters"></a><a id="NOTES_TO_IMPLEMETERS"></a>Notes to Implemeters</h3>
In most cases, resizing only requires that you grow, shrink, or scale your object's frame adornments. However, for more complicated adornments, you may be required to renegotiate for border space with calls to <a href="https://msdn.microsoft.com/7c806a02-db6d-444e-a049-22c4ae2b19b0">IOleInPlaceUIWindow::SetBorderSpace</a> and <b>IOleInPlaceUIWindow::SetBorderSpace</b>.

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceActiveObject::ResizeBorder</b>, do not make calls to the <a href="_win32_PeekMessage_cpp">PeekMessage</a> or <a href="_win32_GetMessage_cpp">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceActiveObject::ResizeBorder</b>.</div>
<div> </div>



## -see-also




<a href="_win32_GetMessage_cpp">GetMessage</a>



<a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a>



<a href="https://msdn.microsoft.com/9ee9970a-b937-4538-b3b8-460647086db1">IOleInPlaceUIWindow::GetBorder</a>



<a href="_win32_PeekMessage_cpp">PeekMessage</a>
 

 

