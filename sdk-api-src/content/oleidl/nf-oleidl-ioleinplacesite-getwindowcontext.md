---
UID: NF:oleidl.IOleInPlaceSite.GetWindowContext
title: IOleInPlaceSite::GetWindowContext (oleidl.h)
author: windows-sdk-content
description: Enables an in-place object to retrieve the window interfaces that form the window object hierarchy, and the position in the parent window where the object's in-place activation window should be located.
old-location: com\ioleinplacesite_getwindowcontext.htm
tech.root: com
ms.assetid: f6cf62b3-5a64-49aa-b0bd-56744ecee313
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetWindowContext, GetWindowContext method [COM], GetWindowContext method [COM],IOleInPlaceSite interface, IOleInPlaceSite interface [COM],GetWindowContext method, IOleInPlaceSite.GetWindowContext, IOleInPlaceSite::GetWindowContext, _ole_ioleinplacesite_getwindowcontext, com.ioleinplacesite_getwindowcontext, oleidl/IOleInPlaceSite::GetWindowContext
ms.topic: method
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
 - IOleInPlaceSite.GetWindowContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceSite::GetWindowContext


## -description


Enables an in-place object to retrieve the window interfaces that form the window object hierarchy, and the position in the parent window where the object's in-place activation window should be located.


## -parameters




### -param ppFrame [out]

A pointer to an <a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a> pointer variable that receives the interface pointer to the frame. If an error occurs, the implementation must set <i>ppFrame</i> to <b>NULL</b>.


### -param ppDoc [out]

A pointer to an <a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a> pointer variable that receives the interface pointer to the document window. If the document window is the same as the frame window, <i>ppDoc</i> is set to <b>NULL</b>. In this case, the object can only use <i>ppFrame</i> or border negotiation. If an error is returned, the implementation must set <i>ppDoc</i> to <b>NULL</b>.


### -param lprcPosRect [out]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure for the rectangle containing the position of the in-place object in the client coordinates of its parent window. If an error is returned, this parameter must be set to <b>NULL</b>.


### -param lprcClipRect [out]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure for the outer rectangle containing the in-place object's position rectangle (<i>lprcPosRect</i>). This rectangle is relative to the client area of the object's parent window. If an error is returned, this parameter must be set to <b>NULL</b>.


### -param lpFrameInfo [in, out]

A pointer to an <a href="https://msdn.microsoft.com/e09445d2-61e5-4691-b51e-746e0cc91c00">OLEINPLACEFRAMEINFO</a> structure the container is to fill in with appropriate data. If an error is returned, this parameter must be set to <b>NULL</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
 One or more of the supplied pointers is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/e09445d2-61e5-4691-b51e-746e0cc91c00">OLEINPLACEFRAMEINFO</a> structure provides data needed by OLE to dispatch keystroke accelerators to a container frame while an object is active in place.

When an object is activated, it calls <b>GetWindowContext</b> from its container. The container returns the handle to its in-place accelerator table through the <a href="https://msdn.microsoft.com/e09445d2-61e5-4691-b51e-746e0cc91c00">OLEINPLACEFRAMEINFO</a> structure. Before calling <b>GetWindowContext</b>, the object must provide the size of the <b>OLEINPLACEFRAMEINFO</b> structure by filling in the cb member, pointed to by <i>lpFrameInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

