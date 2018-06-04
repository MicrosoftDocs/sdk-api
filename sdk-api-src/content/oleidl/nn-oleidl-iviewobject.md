---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IViewObject interface


## -description


Enables an object to display itself directly without passing a data object to the caller. In addition, this interface can create and manage a connection with an advise sink so the caller can be notified of changes in the view object.

The caller can request specific representations and specific target devices. For example, a caller can ask for either an object's content or an iconic representation. Also, the caller can ask the object to compose a picture for a target device that is independent of the drawing device context. As a result, the picture can be composed for one target device and drawn on another device context. For example, to provide a print preview operation, you can compose the drawing for a printer target device but actually draw the representation on the display.

The <b>IViewObject</b> interface is similar to <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>; except that <b>IViewObject</b> places a representation of the data onto a device context while <b>IDataObject</b> places the representation onto a transfer medium.

Unlike most other interfaces, <b>IViewObject</b> cannot be marshaled to another process. This is because device contexts are only effective in the context of one process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IViewObject</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IViewObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IViewObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">Draw</a>
</td>
<td align="left" width="63%">
Draws a representation of the object onto the specified device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">Freeze</a>
</td>
<td align="left" width="63%">
Freezes the drawn representation of an object so that it will not change until a subsequent call to the <a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">Unfreeze</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c56f6cbb-d2ea-4db4-a660-db8b7540ac94">GetAdvise</a>
</td>
<td align="left" width="63%">
Retrieves the advisory connection on the object that was used in the most recent call to <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">SetAdvise</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68454266-ca31-44ec-8847-4d47001d9849">GetColorSet</a>
</td>
<td align="left" width="63%">
Retrieves the logical palette that the object is using for drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">SetAdvise</a>
</td>
<td align="left" width="63%">
Establishes a connection between the view object and an advise sink so that the advise sink can be notified about changes in the object's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">Unfreeze</a>
</td>
<td align="left" width="63%">
Releases a drawing that was previously frozen using <a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">Freeze</a>.

</td>
</tr>
</table> 

