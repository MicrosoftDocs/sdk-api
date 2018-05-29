---
UID: NF:docobj.IOleDocumentView.SetRect
title: IOleDocumentView::SetRect
author: windows-sdk-content
description: Sets the rectangular coordinates of the viewport in which the view is to be activated or resets the coordinates of the viewport in which a view is currently activated.
old-location: com\ioledocumentview_setrect.htm
old-project: com
ms.assetid: 994eddef-65e6-4ccd-92e7-1e76a7c11681
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IOleDocumentView interface [COM],SetRect method, IOleDocumentView.SetRect, IOleDocumentView::SetRect, SetRect, SetRect method [COM], SetRect method [COM],IOleDocumentView interface, _ole_ioledocumentview_setrect, com.ioledocumentview_setrect, docobj/IOleDocumentView::SetRect
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
req.typenames: DOCMISC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DocObj.h
api_name:
-	IOleDocumentView.SetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::SetRect


## -description


Sets the rectangular coordinates of the viewport in which the view is to be activated or resets the coordinates of the viewport in which a view is currently activated.


## -parameters




### -param prcView [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the viewport.


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
</table>
 




## -remarks



For a single document interface (SDI) application, the viewport is the client area of the frame window minus the space allocated for toolbars, status bar, and such. For a multiple document interface (MDI) window, the viewport is the client area of the MDI document window minus any other frame-level user-interface elements.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calling <b>IOleDocumentView::SetRect</b> or <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a> is part of the normal activation sequece for document objects, usually following a call to <a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a> and preceding a call to <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a>.

Whenever the window used to display a document object is resized, the container should call <b>IOleDocumentView::SetRect</b> (or <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>) to tell the document view object to resize itself to the new window dimensions.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The coordinates of the viewport are within the coordinates of the view window, which is obtained through <a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">IOleWindow::GetWindow</a>. The view must resize itself to fit the new coordinates passed in <i>prcView</i>.

This method is defined with the [input_sync] attribute, which means that the view object cannot yield or make another, non input_sync RPC call while executing this method.

A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>
 

 

