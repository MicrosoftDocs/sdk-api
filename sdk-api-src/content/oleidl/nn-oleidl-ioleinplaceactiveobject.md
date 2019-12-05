---
UID: NN:oleidl.IOleInPlaceActiveObject
title: IOleInPlaceActiveObject (oleidl.h)
description: Provides a direct channel of communication between an in-place object and the associated application's outer-most frame window and the document window within the application that contains the embedded object.
old-location: com\ioleinplaceactiveobject.htm
tech.root: com
ms.assetid: b077c256-1109-494c-95c2-2d33bccbe47b
ms.date: 12/05/2018
ms.keywords: IOleInPlaceActiveObject, IOleInPlaceActiveObject interface [COM], IOleInPlaceActiveObject interface [COM],described, _ole_ioleinplaceactiveobject, com.ioleinplaceactiveobject, oleidl/IOleInPlaceActiveObject
ms.topic: interface
f1_keywords:
- oleidl/IOleInPlaceActiveObject
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OleIdl.h
api_name:
- IOleInPlaceActiveObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleInPlaceActiveObject interface


## -description


Provides a direct channel of communication between an in-place object and the associated application's outer-most frame window and the document window within the application that contains the embedded object. The communication involves the translation of messages, the state of the frame window (activated or deactivated), and the state of the document window (activated or deactivated). Also, it informs the object when it needs to resize its borders, and manages modeless dialog boxes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceActiveObject</b> interface inherits from <b>IOleWindow</b>. <b>IOleInPlaceActiveObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceActiveObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-enablemodeless">EnableModeless</a>
</td>
<td align="left" width="63%">
Enables or disables modeless dialog boxes when the container creates or destroys a modal dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate">OnDocWindowActivate</a>
</td>
<td align="left" width="63%">
Notifies the active in-place object when the container's document window is activated or deactivated.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate">OnFrameWindowActivate</a>
</td>
<td align="left" width="63%">
Notifies the object when the container's top-level frame window is activated or deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-resizeborder">ResizeBorder</a>
</td>
<td align="left" width="63%">
Alerts the object that it needs to resize its border space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Processes menu accelerator-key messages from the container's message queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
 

 

