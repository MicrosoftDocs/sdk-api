---
UID: NF:docobj.IOleDocumentView.GetRect
title: IOleDocumentView::GetRect
author: windows-sdk-content
description: Retrieves the rectangular coordinates of the viewport in which the view is or will be activated.
old-location: com\ioledocumentview_getrect.htm
old-project: com
ms.assetid: 65d27354-c278-4d9e-b1b7-6fa3651a343d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: GetRect, GetRect method [COM], GetRect method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],GetRect method, IOleDocumentView.GetRect, IOleDocumentView::GetRect, _ole_ioledocumentview_getrect, com.ioledocumentview_getrect, docobj/IOleDocumentView::GetRect
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
 - IOleDocumentView.GetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::GetRect


## -description


Retrieves the rectangular coordinates of the viewport in which the view is or will be activated.


## -parameters




### -param prcView [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure to contain the coordinates of the current viewport set with <a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a>.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This view has not yet seen a call to <a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a> or <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a> and therefore has no rectangle to return.

</td>
</tr>
</table>
 




## -remarks



For a single document interface (SDI) application, the viewport is the client area of the frame window minus the space allocated for toolbars, status bar, and such. For a multiple document interface (MDI) window, the viewport is the client area of the MDI document window minus any other frame-level user-interface elements.

The viewport coordinates obtained by this method are those set in the most recent call to either <a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a> or <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>.

A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.





## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a>



<a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>
 

 

