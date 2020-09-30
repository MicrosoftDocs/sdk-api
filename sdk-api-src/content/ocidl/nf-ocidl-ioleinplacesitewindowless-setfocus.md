---
UID: NF:ocidl.IOleInPlaceSiteWindowless.SetFocus
title: IOleInPlaceSiteWindowless::SetFocus (ocidl.h)
description: Sets the keyboard focus for a UI-active, windowless object.
helpviewer_keywords: ["IOleInPlaceSiteWindowless interface [COM]","SetFocus method","IOleInPlaceSiteWindowless.SetFocus","IOleInPlaceSiteWindowless::SetFocus","SetFocus","SetFocus method [COM]","SetFocus method [COM]","IOleInPlaceSiteWindowless interface","_ole_ioleinplacesitewindowless_setfocus","com.ioleinplacesitewindowless_setfocus","ocidl/IOleInPlaceSiteWindowless::SetFocus"]
old-location: com\ioleinplacesitewindowless_setfocus.htm
tech.root: com
ms.assetid: 1ea9bade-5e41-49a0-a770-3a5cfc56d0f6
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless interface [COM],SetFocus method, IOleInPlaceSiteWindowless.SetFocus, IOleInPlaceSiteWindowless::SetFocus, SetFocus, SetFocus method [COM], SetFocus method [COM],IOleInPlaceSiteWindowless interface, _ole_ioleinplacesitewindowless_setfocus, com.ioleinplacesitewindowless_setfocus, ocidl/IOleInPlaceSiteWindowless::SetFocus
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
 - IOleInPlaceSiteWindowless::SetFocus
 - ocidl/IOleInPlaceSiteWindowless::SetFocus
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
 - IOleInPlaceSiteWindowless.SetFocus
---

# IOleInPlaceSiteWindowless::SetFocus


## -description

Sets the keyboard focus for a UI-active, windowless object.

## -parameters

### -param fFocus [in]

If <b>TRUE</b>, sets the keyboard focus to the calling object. If <b>FALSE</b>, removes the keyboard focus from the calling object, provided that the object has the focus.

## -returns

This method returns S_OK if the keyboard focus was successfully given to the object. If this method is called to release the focus, it should never fail. Other possible return values include the following.

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
Keyboard focus was denied to the object.

</td>
</tr>
</table>

## -remarks

A windowless object calls this method whenever a windowed object would call the <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">SetFocus</a> function. Through this call, the windowless object obtains the keyboard focus and can respond to window messages. Normally, this call is made during the UI activation process and within the notification methods <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate">IOleInPlaceActiveObject::OnDocWindowActivate</a> with <b>TRUE</b> and <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate">IOleInPlaceActiveObject::OnFrameWindowActivate</a> with <b>TRUE</b>.

In response to this call, the container sets the Windows focus to the window being used to get keyboard messages (usually the container window) and redirects any subsequent keyboard messages to the windowless object that requested the focus.

A windowless object also calls the <b>IOleInPlaceSiteWindowless::SetFocus</b> method with the <i>fFocus</i> parameter set to <b>FALSE</b> to release the keyboard focus without assigning it to any other object. In this case, the container must call the <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">SetFocus</a> function with a <b>NULL</b> parameter so that no window has the focus.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>