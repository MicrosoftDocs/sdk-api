---
UID: NN:oleidl.IOleInPlaceUIWindow
title: IOleInPlaceUIWindow (oleidl.h)
author: windows-sdk-content
description: Implemented by container applications and used by object applications to negotiate border space on the document or frame window.
old-location: com\ioleinplaceuiwindow.htm
tech.root: com
ms.assetid: 3cfb31aa-9746-438c-af64-8236c170fe88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleInPlaceUIWindow, IOleInPlaceUIWindow interface [COM], IOleInPlaceUIWindow interface [COM],described, _ole_ioleinplaceuiwindow, com.ioleinplaceuiwindow, oleidl/IOleInPlaceUIWindow
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
 - IOleInPlaceUIWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleInPlaceUIWindow interface


## -description


Implemented by container applications and used by object applications to negotiate border space on the document or frame window. The container provides a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure in which the object can place toolbars and other similar controls, determines if tools can in fact be installed around the object's window frame, allocates space for the border, and establishes a communication channel between the object and each frame and document window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceUIWindow</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IOleInPlaceUIWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceUIWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">GetBorder</a>
</td>
<td align="left" width="63%">
Retrieves the outer rectange for toolbars and controls while the object is active in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">RequestBorderSpace</a>
</td>
<td align="left" width="63%">
Determines whether there is space available for tools to be installed around object's window frame while the object is active in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setactiveobject">SetActiveObject</a>
</td>
<td align="left" width="63%">
Provides a direct channel of communication between the object and each of the frame and document windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">SetBorderSpace</a>
</td>
<td align="left" width="63%">
Allocates space for the border requested in the call to <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-requestborderspace">RequestBorderSpace</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
 

 

