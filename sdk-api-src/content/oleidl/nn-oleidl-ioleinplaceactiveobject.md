---
UID: NN:oleidl.IOleInPlaceActiveObject
title: IOleInPlaceActiveObject
author: windows-driver-content
description: Provides a direct channel of communication between an in-place object and the associated application's outer-most frame window and the document window within the application that contains the embedded object.
old-location: com\ioleinplaceactiveobject.htm
old-project: com
ms.assetid: b077c256-1109-494c-95c2-2d33bccbe47b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IOleInPlaceActiveObject, IOleInPlaceActiveObject interface [COM], IOleInPlaceActiveObject interface [COM],described, _ole_ioleinplaceactiveobject, com.ioleinplaceactiveobject, oleidl/IOleInPlaceActiveObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IOleInPlaceActiveObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/2fc45490-b3fe-48fd-a41c-2b7f35b09edc">EnableModeless</a>
</td>
<td align="left" width="63%">
Enables or disables modeless dialog boxes when the container creates or destroys a modal dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8333d707-4d34-4a87-9990-b25597ffa9fc">OnDocWindowActivate</a>
</td>
<td align="left" width="63%">
Notifies the active in-place object when the container's document window is activated or deactivated.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6534ea03-5f1b-4d3e-b6d8-b8d478a0a144">OnFrameWindowActivate</a>
</td>
<td align="left" width="63%">
Notifies the object when the container's top-level frame window is activated or deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/240d2ae5-abce-4bea-969e-f47780908bbb">ResizeBorder</a>
</td>
<td align="left" width="63%">
Alerts the object that it needs to resize its border space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce460c52-c7aa-4ee4-955e-76407af7cf1e">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Processes menu accelerator-key messages from the container's message queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>
 

 

