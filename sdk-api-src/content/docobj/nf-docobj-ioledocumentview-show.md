---
UID: NF:docobj.IOleDocumentView.Show
title: IOleDocumentView::Show
author: windows-sdk-content
description: Activates or deactivates a view.
old-location: com\ioledocumentview_show.htm
old-project: com
ms.assetid: eecc0230-0713-40e9-913c-c51b8a905575
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IOleDocumentView interface [COM],Show method, IOleDocumentView.Show, IOleDocumentView::Show, Show, Show method [COM], Show method [COM],IOleDocumentView interface, _ole_ioledocumentview_show, com.ioledocumentview_show, docobj/IOleDocumentView::Show
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
 - IOleDocumentView.Show
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::Show


## -description


Activates or deactivates a view.


## -parameters




### -param fShow [in]

If <b>TRUE</b>, the view is to show itself. If <b>FALSE</b>, the view is to hide itself.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for operation.

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



Calling <b>Show</b> is the last step in the activation sequence, because before showing itself a document object must know exactly what space it occupies and have all its tools available.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A call to this method for the purpose of activating a view should follow calls to <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>, <a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a>, and <a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a> (or <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>).

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementations of this method should embody the following pseudocode.

<pre class="syntax" xml:space="preserve"><code>if (fShow)
    {
    In-place activate the view but do not UI activate it.
    Show the view window. 
    }
else
    {
    Call IOleDocumentView::UIActivate(FALSE) on this view
    Hide the view window
    }</code></pre>
All views of a document object must at least support in-place activation; E_NOTIMPL is not an acceptable value.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>



<a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a>



<a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>



<a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a>
 

 

