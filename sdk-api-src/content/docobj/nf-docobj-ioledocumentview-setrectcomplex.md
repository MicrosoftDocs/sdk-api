---
UID: NF:docobj.IOleDocumentView.SetRectComplex
title: IOleDocumentView::SetRectComplex
author: windows-sdk-content
description: Sets the rectangular coordinates of the viewport, scroll bars, and size box.
old-location: com\ioledocumentview_setrectcomplex.htm
old-project: com
ms.assetid: d220b200-85cb-43ff-a59d-147c14eef544
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IOleDocumentView interface [COM],SetRectComplex method, IOleDocumentView.SetRectComplex, IOleDocumentView::SetRectComplex, SetRectComplex, SetRectComplex method [COM], SetRectComplex method [COM],IOleDocumentView interface, _ole_ioledocumentview_setrectcomplex, com.ioledocumentview_setrectcomplex, docobj/IOleDocumentView::SetRectComplex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DOCMISC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocumentView.SetRectComplex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::SetRectComplex


## -description


Sets the rectangular coordinates of the viewport, scroll bars, and size box.


## -parameters




### -param prcView [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the viewport.


### -param prcHScroll [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the horizontal scroll bar.


### -param prcVScroll [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the vertical scroll bar.


### -param prcSizeBox [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the size box.


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
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The document object that owns this view does not support complex rectangles.

</td>
</tr>
</table>
 




## -remarks



View frames that support a workbook metaphor, in which a single document comprises multiple sheets or pages, typically call this method to set the coordinates to be used in common by all the sheets or pages.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calling <b>IOleDocumentView::SetRectComplex</b> is part of the normal activation sequence for document objects that support complex rectangles, usually following a call to <a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a> and preceding a call to <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a>.

Whenever the window used to display a document object is resized, the container should call <b>IOleDocumentView::SetRectComplex</b> or <a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a> to tell the view object to resize itself to the new window dimensions.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Document objects that support complex rectangles mark themselves with <a href="https://msdn.microsoft.com/e52e022e-dd82-42f0-a3dd-2730ad80613c">DOCMISC</a>_SUPPORTCOMPLEXRECTANGLES, as described in <b>DOCMISC</b> and <a href="https://msdn.microsoft.com/de279d46-057e-4c3a-8af3-14f7b65147fd">IOleDocument::GetDocMiscStatus</a>. Document objects that do not support this method can return E_NOTIMPL.

Upon receiving a call to this method, a view should resize itself to fit the coordinates specified in prcView and fit its scrollbars and size box to the areas described in <i>prcHScroll</i>, <i>prcVScroll</i>, and <i>prcSizeBox</i>.

This method is defined with the [input_sync] attribute, which means that the implementing object cannot yield or make another, non input_sync RPC call while executing this method.




## -see-also




<a href="https://msdn.microsoft.com/de279d46-057e-4c3a-8af3-14f7b65147fd">IOleDocument::GetDocMiscStatus</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>
 

 

