---
UID: NN:ocidl.IOleInPlaceSiteWindowless
title: IOleInPlaceSiteWindowless
author: windows-sdk-content
description: Extends the IOleInPlaceSiteEx interface.
old-location: com\ioleinplacesitewindowless.htm
tech.root: com
ms.assetid: 4ad83599-99d2-4b35-95de-cff845a8d5e4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IOleInPlaceSiteWindowless, IOleInPlaceSiteWindowless interface [COM], IOleInPlaceSiteWindowless interface [COM],described, _ole_ioleinplacesitewindowless, com.ioleinplacesitewindowless, ocidl/IOleInPlaceSiteWindowless
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IOleInPlaceSiteWindowless
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceSiteWindowless interface


## -description


Extends the <a href="https://msdn.microsoft.com/d93e6d23-7867-43e4-8ab9-efe609362c18">IOleInPlaceSiteEx</a> interface. <b>IOleInPlaceSiteWindowless</b> works with <a href="https://msdn.microsoft.com/86aabb46-6bc7-4953-b4eb-8692552ca380">IOleInPlaceObjectWindowless</a> which is implemented on the windowless object. Together, these two interfaces provide services to a windowless object from its container allowing the windowless object to:
<ul>
<li>Process window messages</li>
<li>Participate in drag and drop operations
</li>
<li>Perform drawing operations</li>
</ul>Having a window can place unnecessary burdens on small objects, such as controls. It prevents an object from being non-rectangular. It prevents windows from being transparent. It prevents the small instance size needed by many small controls.

A windowless object can enter the in-place active state without requiring a window or the resources associated with a window. Instead, the object's container provides the object with many of the services associated with having a window.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceSiteWindowless</b> interface inherits from <b>IOleInPlaceSiteEx</b>. <b>IOleInPlaceSiteWindowless</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceSiteWindowless</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36fa395d-09b2-474d-85ae-5a22d25e88eb">AdjustRect</a>
</td>
<td align="left" width="63%">
Adjusts a specified rectangle if it is entirely or partially covered by overlapping, opaque objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e2f2820-e8d7-4f0e-921d-4fc88feca15f">CanWindowlessActivate</a>
</td>
<td align="left" width="63%">
Informs an object if its container can support it as a windowless object that can be in-place activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adbe9c66-d716-4489-b705-43a5317c7646">GetCapture</a>
</td>
<td align="left" width="63%">
Called by an in-place active, windowless object to determine whether it still has the mouse capture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">GetDC</a>
</td>
<td align="left" width="63%">
Provides an object with a handle to a device context for a screen or compatible device from its container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/282f350c-d196-40c2-880f-55f28dc48f2b">GetFocus</a>
</td>
<td align="left" width="63%">
Called by an in-place active, windowless object to determine whether it still has the keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/034025f5-f9cd-4ad3-9b98-216b373cd10f">InvalidateRect</a>
</td>
<td align="left" width="63%">
Enables an object to invalidate a specified rectangle of its in-place image on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe86f4f-d023-4285-a6c1-c42fdc566f2f">InvalidateRgn</a>
</td>
<td align="left" width="63%">
Enables an object to invalidate a specified region of its in-place image on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14017061-57e3-49a9-93cc-6373522ab1dc">OnDefWindowMessage</a>
</td>
<td align="left" width="63%">
Invokes the default processing for all messages passed to an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8778a58c-2995-4c14-826c-9c97e97e957b">ReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the device context previously obtained by a call to <a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">IOleInPlaceSiteWindowless::GetDC</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eeb1aee-8cd4-4d27-8b6f-f76305bbe69f">ScrollRect</a>
</td>
<td align="left" width="63%">
Enables an object to scroll an area within its in-place active image on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48de7ab3-eb1e-49e1-8d31-ca1ef1f9055d">SetCapture</a>
</td>
<td align="left" width="63%">
Enables an in-place active, windowless object to capture all mouse messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea9bade-5e41-49a0-a770-3a5cfc56d0f6">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the keyboard focus for a UI-active, windowless object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d1a52353-dd86-4083-9dbc-3a6f363a1a57">IAdviseSinkEx</a>



<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>



<a href="https://msdn.microsoft.com/ce460c52-c7aa-4ee4-955e-76407af7cf1e">IOleInPlaceActiveObject::TranslateAccelerator</a>



<a href="https://msdn.microsoft.com/86aabb46-6bc7-4953-b4eb-8692552ca380">IOleInPlaceObjectWindowless</a>
 

 

