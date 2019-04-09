---
UID: NF:ocidl.IPointerInactive.OnInactiveMouseMove
title: IPointerInactive::OnInactiveMouseMove (ocidl.h)
author: windows-sdk-content
description: Notifies the object that the mouse pointer has moved over it so the object can fire mouse events. This method is called by the container on receipt of a WM_MOUSEMOVE method when an inactive object is under the mouse pointer.
old-location: com\ipointerinactive_oninactivemousemove.htm
tech.root: com
ms.assetid: d026c570-b51b-456f-b121-eb2be08e2cac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPointerInactive interface [COM],OnInactiveMouseMove method, IPointerInactive.OnInactiveMouseMove, IPointerInactive::OnInactiveMouseMove, OnInactiveMouseMove, OnInactiveMouseMove method [COM], OnInactiveMouseMove method [COM],IPointerInactive interface, _ctrl_ipointerinactive_oninactivemousemove, com.ipointerinactive_oninactivemousemove, ocidl/IPointerInactive::OnInactiveMouseMove
ms.topic: method
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
 - IPointerInactive.OnInactiveMouseMove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPointerInactive::OnInactiveMouseMove


## -description


Notifies the object that the mouse pointer has moved over it so the object can fire mouse events. This method is called by the container on receipt of a WM_MOUSEMOVE method when an inactive object is under the mouse pointer.


## -parameters




### -param pRectBounds [in]

The object bounding rectangle, in client coordinates of the containing window. This parameter tells the object its exact position and size on the screen when the WM_MOUSEMOVE message was received. This value is specified in units of the client's coordinate system.


### -param x [in]

The horizontal coordinate of mouse location in units of the client's containing window.


### -param y [in]

The vertical coordinate of mouse location in units of the client's containing window.


### -param grfKeyState [in]

The current state of the keyboard modifier keys on the keyboard. Possible values can be a combination of any of the values MK_CONTROL, MK_SHIFT, MK_ALT, MK_BUTTON, MK_LBUTTON, MK_MBUTTON, and MK_RBUTTON.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



The container calls this method to notify the object that the mouse pointer is over the object after checking the object's activation policy by calling the <a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a> method. If the object has not requested to be activated in-place through that call, the container dispatches subsequent WM_MOUSEMOVE messages to the inactive object by calling <b>OnInactiveMouseMove</b> as long as the mouse pointer stays over the object. The object can then fire mouse move events.

To avoid rounding errors and to make the job easier on the object implementer, this method takes window coordinates in the units of its containing client window, that is, the window in which the object is displayed, instead of the usual <b>HIMETRIC</b> units. Thus, the same coordinates and code path can be used when the object is active and inactive. The window coordinates specify the mouse position. The bounding rectangle is also specified in the same coordinate system.




## -see-also




<a href="https://msdn.microsoft.com/dc08d512-6994-419a-a460-6274ce74e40f">IPointerInactive</a>
 

 

