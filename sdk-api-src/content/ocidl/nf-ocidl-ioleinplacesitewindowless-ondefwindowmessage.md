---
UID: NF:ocidl.IOleInPlaceSiteWindowless.OnDefWindowMessage
title: IOleInPlaceSiteWindowless::OnDefWindowMessage (ocidl.h)
description: Invokes the default processing for all messages passed to an object.
helpviewer_keywords: ["IOleInPlaceSiteWindowless interface [COM]","OnDefWindowMessage method","IOleInPlaceSiteWindowless.OnDefWindowMessage","IOleInPlaceSiteWindowless::OnDefWindowMessage","OnDefWindowMessage","OnDefWindowMessage method [COM]","OnDefWindowMessage method [COM]","IOleInPlaceSiteWindowless interface","_ole_ioleinplacesitewindowless_ondefwindowmessage","com.ioleinplacesitewindowless_ondefwindowmessage","ocidl/IOleInPlaceSiteWindowless::OnDefWindowMessage"]
old-location: com\ioleinplacesitewindowless_ondefwindowmessage.htm
tech.root: com
ms.assetid: 14017061-57e3-49a9-93cc-6373522ab1dc
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless interface [COM],OnDefWindowMessage method, IOleInPlaceSiteWindowless.OnDefWindowMessage, IOleInPlaceSiteWindowless::OnDefWindowMessage, OnDefWindowMessage, OnDefWindowMessage method [COM], OnDefWindowMessage method [COM],IOleInPlaceSiteWindowless interface, _ole_ioleinplacesitewindowless_ondefwindowmessage, com.ioleinplacesitewindowless_ondefwindowmessage, ocidl/IOleInPlaceSiteWindowless::OnDefWindowMessage
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
 - IOleInPlaceSiteWindowless::OnDefWindowMessage
 - ocidl/IOleInPlaceSiteWindowless::OnDefWindowMessage
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
 - IOleInPlaceSiteWindowless.OnDefWindowMessage
---

# IOleInPlaceSiteWindowless::OnDefWindowMessage


## -description

Invokes the default processing for all messages passed to an object.

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
The container's default processing for the window message was not invoked. See Note to Implementers below.

</td>
</tr>
</table>

## -remarks

A windowless object can explicitly invoke the default processing for a window message by calling this method. A container dispatches window messages to its windowless objects by calling <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless::OnWindowMessage</a>. The object usually returns S_FALSE to indicate that it did not process the message. Then, the container can perform the default behavior for the message by calling the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function.

Instead, the object can call this method on the container's site object to explicitly invoke the default processing. Then, the object can take action on its own if the container does not handle the message.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The container must pass the following window messages to its default window procedure (the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function) and return S_OK. Note that *<i>plResult</i> should contain the value returned by <b>DefWindowProc</b>.

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
The container can either process the window messages as its own and return S_OK or not do anything and return S_FALSE.

<ul>
<li>WM_CONTEXTMENU</li>
<li>WM_HELP</li>
<li>WM_SETCURSOR</li>
</ul>
If the container returns S_FALSE, the object can take action to process the window message on its own.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless::OnWindowMessage</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>