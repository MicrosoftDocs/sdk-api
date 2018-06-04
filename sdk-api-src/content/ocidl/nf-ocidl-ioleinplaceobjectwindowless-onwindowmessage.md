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

# IOleInPlaceObjectWindowless::OnWindowMessage


## -description


Dispatches a message from a container to a windowless object that is in-place active.


## -parameters




### -param msg [in]

The identifier for the window message provided to the container by Windows.


### -param wParam [in]

A parameter for the window message provided to the container by Windows.


### -param lParam [in]

A parameter for the window message provided to the container by Windows.


### -param plResult [out]

A pointer to result code for the window message.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The windowless object did not process the window message. The container should call the DefWindowProc for the message or process the message itself as described below.

</td>
</tr>
</table>
 




## -remarks



A container calls this method to send window messages to a windowless object that is in-place active. The container should dispatch messages according to the following guidelines:

For the following messages, the container should first dispatch the message to the windowless object that has captured the mouse, if any. Otherwise, the container should dispatch the message to the windowless object under the mouse cursor. If there is no such object, the container is free to process the following messages for itself:

<ul>
<li>WM_MOUSEMOVE</li>
<li>WM_SETCURSOR</li>
<li>WM_XBUTTONDOWN</li>
<li>WM_XBUTTONUP</li>
<li>WM_XBUTTONDBLCLK</li>
</ul>
The container should dispatch the message to the windowless object with the keyboard focus for the following messages:

<ul>
<li>WM_CANCELMODE</li>
<li>WM_CHAR</li>
<li>WM_DEADCHAR</li>
<li>WM_HELP</li>
<li>WM_IMExxx</li>
<li>WM_KEYDOWN</li>
<li>WM_KEYUP</li>
<li>WM_SYSDEADCHAR</li>
<li>WM_SYSKEYDOWN</li>
<li>WM_SYSKEYUP</li>
</ul>
For all other messages, the container should process the message on its own.

The windowless object can return S_FALSE to this method to indicate that it did not process the message. Then, the container either performs the default behavior for the message by calling the <a href="_win32_DefWindowProc_cpp">DefWindowProc</a> function, or processes the message itself.

The container must pass the following window messages to the default window procedure:

<ul>
<li>WM_CHAR</li>
<li>WM_DEADCHAR</li>
<li>WM_IMExxx</li>
<li>WM_KEYDOWN</li>
<li>WM_KEYUP</li>
<li>WM_MOUSEMOVE</li>
<li>WM_SYSCHAR</li>
<li>WM_SYSDEADCHAR</li>
<li>WM_SYSKEYUP</li>
<li>WM_XBUTTONDOWN</li>
<li>WM_XBUTTONUP</li>
<li>WM_XBUTTONDBLCLK</li>
</ul>
The container must process the following window messages as its own:

<ul>
<li>WM_CONTEXTMENU</li>
<li>WM_HELP</li>
<li>WM_SETCURSOR</li>
</ul>
<div class="alert"><b>Note</b>  For WM_SETCURSOR, the container can either set the cursor itself or do nothing.</div>
<div> </div>
Objects can also use <a href="https://msdn.microsoft.com/14017061-57e3-49a9-93cc-6373522ab1dc">IOleInPlaceSiteWindowless::OnDefWindowMessage</a> to explicitly invoke the default message processing from the container. In the case of the WM_SETCURSOR message, this allows an object to take action if the container does not set the cursor.

All coordinates passed to the object in <i>wParam</i> and <i>lParam</i> are specified as client coordinates of the containing window.




## -see-also




<a href="https://msdn.microsoft.com/86aabb46-6bc7-4953-b4eb-8692552ca380">IOleInPlaceObjectWindowless</a>



<a href="https://msdn.microsoft.com/14017061-57e3-49a9-93cc-6373522ab1dc">IOleInPlaceSiteWindowless::OnDefWindowMessage</a>



<a href="https://msdn.microsoft.com/48de7ab3-eb1e-49e1-8d31-ca1ef1f9055d">IOleInPlaceSiteWindowless:SetCapture</a>
 

 

