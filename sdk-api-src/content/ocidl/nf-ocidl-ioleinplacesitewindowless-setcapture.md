---
UID: NF:ocidl.IOleInPlaceSiteWindowless.SetCapture
title: IOleInPlaceSiteWindowless::SetCapture (ocidl.h)
description: Enables an in-place active, windowless object to capture all mouse messages.
helpviewer_keywords: ["IOleInPlaceSiteWindowless interface [COM]","SetCapture method","IOleInPlaceSiteWindowless.SetCapture","IOleInPlaceSiteWindowless::SetCapture","SetCapture","SetCapture method [COM]","SetCapture method [COM]","IOleInPlaceSiteWindowless interface","_ole_ioleinplacesitewindowless_setcapture","com.ioleinplacesitewindowless_setcapture","ocidl/IOleInPlaceSiteWindowless::SetCapture"]
old-location: com\ioleinplacesitewindowless_setcapture.htm
tech.root: com
ms.assetid: 48de7ab3-eb1e-49e1-8d31-ca1ef1f9055d
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless interface [COM],SetCapture method, IOleInPlaceSiteWindowless.SetCapture, IOleInPlaceSiteWindowless::SetCapture, SetCapture, SetCapture method [COM], SetCapture method [COM],IOleInPlaceSiteWindowless interface, _ole_ioleinplacesitewindowless_setcapture, com.ioleinplacesitewindowless_setcapture, ocidl/IOleInPlaceSiteWindowless::SetCapture
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleInPlaceSiteWindowless::SetCapture
 - ocidl/IOleInPlaceSiteWindowless::SetCapture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceSiteWindowless.SetCapture
---

# IOleInPlaceSiteWindowless::SetCapture


## -description

Enables an in-place active, windowless object to capture all mouse messages.

## -parameters

### -param fCapture [in]

If <b>TRUE</b>, the container should capture the mouse for the object. If <b>FALSE</b>, the container should release mouse capture for the object.

## -returns

This method returns S_OK if the mouse capture was successfully granted to the object. If called to release the mouse capture, this method must not fail. Other possible return values include the following.

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
Mouse capture was denied to the object.


</td>
</tr>
</table>

## -remarks

A windowless object captures the mouse input, by calling <b>IOleInPlaceSiteWindowless::SetCapture</b> with <b>TRUE</b> on its site object. The container can deny mouse capture, in which case this method returns S_FALSE. If the capture is granted, the container must set the Windows mouse capture to its own window and dispatch any subsequent mouse message to the object, regardless of whether the mouse cursor position is over this object or not.

The object can later release mouse capture by calling <b>IOleInPlaceSiteWindowless::SetCapture</b> with <b>FALSE</b> on its site object. The capture can also be released because of an external event, such as the ESC key being pressed. In this case, the object is notified by a <a href="/windows/desktop/winmsg/wm-cancelmode">WM_CANCELMODE</a> message that the container dispatches along with the keyboard focus.



Containers should dispatch all mouse messages, including <a href="/windows/desktop/menurc/wm-setcursor">WM_SETCURSOR</a>, to the windowless OLE object that has captured the mouse. If no object has captured the mouse, the container should dispatch the mouse message to the object under the mouse cursor.

The container dispatches these window messages by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplaceobjectwindowless-onwindowmessage">IOleInPlaceObjectWindowless::OnWindowMessage</a> on the windowless object. The windowless object can return S_FALSE to this method to indicate that it did not process the mouse message. Then, the container should perform the default behavior for the message by calling the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function. For <a href="/windows/desktop/menurc/wm-setcursor">WM_SETCURSOR</a>, the container can either set the cursor itself or do nothing.

Objects can also use <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-ondefwindowmessage">IOleInPlaceSiteWindowless::OnDefWindowMessage</a> to invoke the default message processing from the container. In the case of the <a href="/windows/desktop/menurc/wm-setcursor">WM_SETCURSOR</a> message, this allows an object to take action if the container does not set the cursor.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-ondefwindowmessage">IOleInPlaceSiteWindowless::OnDefWindowMessage</a>