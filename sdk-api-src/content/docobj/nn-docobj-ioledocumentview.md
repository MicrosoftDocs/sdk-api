---
UID: NN:docobj.IOleDocumentView
title: IOleDocumentView
author: windows-sdk-content
description: The IOleDocumentView interface enables a container to communicate with each view supported by a document object.
old-location: com\ioledocumentview.htm
tech.root: com
ms.assetid: 07948c08-f047-4ae0-a41b-5410b4bbf4d6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IOleDocumentView, IOleDocumentView interface [COM], IOleDocumentView interface [COM],described, _ole_ioledocumentview, com.ioledocumentview, docobj/IOleDocumentView
ms.prod: windows
ms.technology: windows-sdk
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
---

# IOleDocumentView interface


## -description


The <b>IOleDocumentView</b> interface enables a container to communicate with each view supported by a document object.

A document object that supports multiple views of its data represents each view as a separate object. Each document view object implements <b>IOleDocumentView</b>, along with <a href="https://msdn.microsoft.com/c14de79d-e844-49cf-ae70-6c3e417fab90">IOleInPlaceObject</a>, <a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a>, and optional interfaces such as <a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a> and <a href="https://msdn.microsoft.com/5c8b455e-7740-4f71-aef6-27390a11a1a3">IOleCommandTarget</a>. A document object that supports only a single view does not require that view to be implemented as a separate object. Instead, both document and view can be implemented as a single class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleDocumentView</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleDocumentView</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f78526b4-977a-4dde-8a2f-7ae0a1c5c7f9">ApplyViewState</a>
</td>
<td align="left" width="63%">
Initializes a view with view state previously saved in call to <a href="https://msdn.microsoft.com/d270b441-d0d5-4dd5-995b-6ca5738747c5">IOleDocumentView::SaveViewState</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8acc469-26f6-4f1b-94a5-4839aa235a1d">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2f443de-929e-4bd4-bfb3-2a28c119c176">CloseView</a>
</td>
<td align="left" width="63%">
Instructs a view to close itself and releases its <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46174e4f-c943-4e70-af68-79363962cdee">GetDocument</a>
</td>
<td align="left" width="63%">
Obtains the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer of the document object that owns this view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d48cd54c-11b3-4acd-a13a-75a612f1761a">GetInPlaceSite</a>
</td>
<td align="left" width="63%">
Retrieves the view site associated with this view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65d27354-c278-4d9e-b1b7-6fa3651a343d">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangular coordinates of the viewport in which the view is or will be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f801ae-ae03-4567-9442-cf3fbb6d06d7">Open</a>
</td>
<td align="left" width="63%">
Displays a document view in a separate pop-up window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d270b441-d0d5-4dd5-995b-6ca5738747c5">SaveViewState</a>
</td>
<td align="left" width="63%">
Saves the view state into the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">SetInPlaceSite</a>
</td>
<td align="left" width="63%">
Associates a container's document view site with a document's  view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/994eddef-65e6-4ccd-92e7-1e76a7c11681">SetRect</a>
</td>
<td align="left" width="63%">
Sets the rectangular coordinates of the viewport in which the view is to be activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">SetRectComplex</a>
</td>
<td align="left" width="63%">
Sets the rectangular coordinates of the viewport, scroll bars, and size box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">Show</a>
</td>
<td align="left" width="63%">
Activates or deactivates a view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">UIActivate</a>
</td>
<td align="left" width="63%">
Activates or deactivates a document view's user interface elements, such as menus, toolbars, and accelerators.

</td>
</tr>
</table> 

