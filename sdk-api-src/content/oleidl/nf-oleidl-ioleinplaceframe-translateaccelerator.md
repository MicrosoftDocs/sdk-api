---
UID: NF:oleidl.IOleInPlaceFrame.TranslateAccelerator
title: IOleInPlaceFrame::TranslateAccelerator (oleidl.h)
description: Translates accelerator keystrokes intended for the container's frame while an object is active in place.
helpviewer_keywords: ["IOleInPlaceFrame interface [COM]","TranslateAccelerator method","IOleInPlaceFrame.TranslateAccelerator","IOleInPlaceFrame::TranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [COM]","TranslateAccelerator method [COM]","IOleInPlaceFrame interface","_ole_ioleinplaceframe_translateaccelerator","com.ioleinplaceframe_translateaccelerator","oleidl/IOleInPlaceFrame::TranslateAccelerator"]
old-location: com\ioleinplaceframe_translateaccelerator.htm
tech.root: com
ms.assetid: f755b919-b810-4b66-b3c2-bf38bd525d60
ms.date: 12/05/2018
ms.keywords: IOleInPlaceFrame interface [COM],TranslateAccelerator method, IOleInPlaceFrame.TranslateAccelerator, IOleInPlaceFrame::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IOleInPlaceFrame interface, _ole_ioleinplaceframe_translateaccelerator, com.ioleinplaceframe_translateaccelerator, oleidl/IOleInPlaceFrame::TranslateAccelerator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleInPlaceFrame::TranslateAccelerator
 - oleidl/IOleInPlaceFrame::TranslateAccelerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceFrame.TranslateAccelerator
---

# IOleInPlaceFrame::TranslateAccelerator


## -description

Translates accelerator keystrokes intended for the container's frame while an object is active in place.

## -parameters

### -param lpmsg [in]

A pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains the keystroke message.

### -param wID [in]

The command identifier value corresponding to the keystroke in the container-provided accelerator table. Containers should use this value instead of translating again.

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
The keystroke was not used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <b>IOleInPlaceFrame::TranslateAccelerator</b> method is called indirectly by <a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a> when a keystroke accelerator intended for the container (frame) is received.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The container application should perform its usual accelerator processing, or use <i>wID</i> directly, and then return, indicating whether the keystroke accelerator was processed. If the container is an MDI application and the <a href="/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a> function fails, the container can call the <a href="/windows/desktop/api/winuser/nf-winuser-translatemdisysaccel">TranslateMDISysAccel</a> function, just as it does for its usual message processing.

In-place objects should be given first chance at translating accelerator messages. However, because objects implemented by DLL object applications do not have their own message pump, they receive their messages from the container's message queue. To ensure that the object has first chance at translating messages, a container should always call <b>IOleInPlaceFrame::TranslateAccelerator</b> before doing its own accelerator translation. Conversely, an executable object application should call <a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a> after calling <a href="/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a>, calling <a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> and <a href="/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a> only if both translation functions fail.

You should define accelerator tables for containers so they will work properly with object applications that do their own accelerator keystroke translations. Tables should be defined as follows.


``` syntax
"char", wID, VIRTKEY, CONTROL
```

This is the most common way to describe keyboard accelerators. Failure to do so can result in keystrokes being lost or sent to the wrong object during an in-place session.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-translateaccelerator">IOleInPlaceFrame::TranslateAccelerator</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>



<a href="/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a>



<a href="/windows/desktop/api/winuser/nf-winuser-translatemdisysaccel">TranslateMDISysAccel</a>
