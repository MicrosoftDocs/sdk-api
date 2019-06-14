---
UID: NN:docobj.IOleDocumentView
title: IOleDocumentView (docobj.h)
author: windows-sdk-content
description: The IOleDocumentView interface enables a container to communicate with each view supported by a document object.
old-location: com\ioledocumentview.htm
tech.root: com
ms.assetid: 07948c08-f047-4ae0-a41b-5410b4bbf4d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleDocumentView, IOleDocumentView interface [COM], IOleDocumentView interface [COM],described, _ole_ioledocumentview, com.ioledocumentview, docobj/IOleDocumentView
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocumentView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleDocumentView interface


## -description


The <b>IOleDocumentView</b> interface enables a container to communicate with each view supported by a document object.

A document object that supports multiple views of its data represents each view as a separate object. Each document view object implements <b>IOleDocumentView</b>, along with <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>, <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>, and optional interfaces such as <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a> and <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a>. A document object that supports only a single view does not require that view to be implemented as a separate object. Instead, both document and view can be implemented as a single class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleDocumentView</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleDocumentView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleDocumentView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-applyviewstate">ApplyViewState</a>
</td>
<td align="left" width="63%">
Initializes a view with view state previously saved in call to <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-saveviewstate">IOleDocumentView::SaveViewState</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-closeview">CloseView</a>
</td>
<td align="left" width="63%">
Instructs a view to close itself and releases its <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-getdocument">GetDocument</a>
</td>
<td align="left" width="63%">
Obtains the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of the document object that owns this view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-getinplacesite">GetInPlaceSite</a>
</td>
<td align="left" width="63%">
Retrieves the view site associated with this view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-getrect">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangular coordinates of the viewport in which the view is or will be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-open">Open</a>
</td>
<td align="left" width="63%">
Displays a document view in a separate pop-up window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-saveviewstate">SaveViewState</a>
</td>
<td align="left" width="63%">
Saves the view state into the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">SetInPlaceSite</a>
</td>
<td align="left" width="63%">
Associates a container's document view site with a document's  view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrect">SetRect</a>
</td>
<td align="left" width="63%">
Sets the rectangular coordinates of the viewport in which the view is to be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">SetRectComplex</a>
</td>
<td align="left" width="63%">
Sets the rectangular coordinates of the viewport, scroll bars, and size box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-show">Show</a>
</td>
<td align="left" width="63%">
Activates or deactivates a view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-uiactivate">UIActivate</a>
</td>
<td align="left" width="63%">
Activates or deactivates a document view's user interface elements, such as menus, toolbars, and accelerators.

</td>
</tr>
</table> 

