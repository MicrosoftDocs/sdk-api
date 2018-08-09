---
UID: NF:docobj.IOleDocumentView.UIActivate
title: IOleDocumentView::UIActivate
author: windows-sdk-content
description: Activates or deactivates a document view's user interface elements, such as menus, toolbars, and accelerators.
old-location: com\ioledocumentview_uiactivate.htm
old-project: com
ms.assetid: df92366c-89b3-44b3-bea0-1b6deb321fe4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleDocumentView interface [COM],UIActivate method, IOleDocumentView.UIActivate, IOleDocumentView::UIActivate, UIActivate, UIActivate method [COM], UIActivate method [COM],IOleDocumentView interface, _ole_ioledocumentview_uiactivate, com.ioledocumentview_uiactivate, docobj/IOleDocumentView::UIActivate
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
 - IOleDocumentView.UIActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::UIActivate


## -description


Activates or deactivates a document view's user interface elements, such as menus, toolbars, and accelerators.


## -parameters




### -param fUIActivate [in]

If <b>TRUE</b>, the view is to activate its user interface. If <b>FALSE</b>, the view is to deactivate its user interface.


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



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calling this method before calling <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a> returns E_UNEXPECTED, because the view must be associated with a view site before it can activate itself.

When <b>IOleDocumentView::UIActivate</b> is called as part of the activation sequence, the call should precede a call to <a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a> or <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>, because otherwise the view dimensions would not account for toolbar space.

To deactivate a view, the container should call <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a> with <b>FALSE</b>, followed by <b>IOleDocumentView::UIActivate</b> with <b>FALSE</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementations of this method should embody the following pseudocode.

<pre class="syntax" xml:space="preserve"><code>if (fActivate)
    {
    UI activate the view (do menu merging, show frame level tools, process accelerators)
    Take focus, and bring the view window forward.
    }
else
    call IOleInPlaceObject::UIDeactivate on this view</code></pre>
In addition, the view can and should participate in extended <b>Help</b> menu merging.

All views of a document object must support in-place activation. E_NOTIMPL is not an acceptable return value.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>



<a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">IOleDocumentView::SetRect</a>



<a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>



<a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a>
 

 

