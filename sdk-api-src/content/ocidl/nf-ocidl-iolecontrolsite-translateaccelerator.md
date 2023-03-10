---
UID: NF:ocidl.IOleControlSite.TranslateAccelerator
title: IOleControlSite::TranslateAccelerator (ocidl.h)
description: Passes a keystroke to the control site for processing.
helpviewer_keywords: ["IOleControlSite interface [COM]","TranslateAccelerator method","IOleControlSite.TranslateAccelerator","IOleControlSite::TranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [COM]","TranslateAccelerator method [COM]","IOleControlSite interface","_ctrl_iolecontrolsite_translateaccelerator","com.iolecontrolsite_translateaccelerator","ocidl/IOleControlSite::TranslateAccelerator"]
old-location: com\iolecontrolsite_translateaccelerator.htm
tech.root: com
ms.assetid: e4f9a6f7-bb0f-41d2-b1b8-7fda2dbee278
ms.date: 12/05/2018
ms.keywords: IOleControlSite interface [COM],TranslateAccelerator method, IOleControlSite.TranslateAccelerator, IOleControlSite::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IOleControlSite interface, _ctrl_iolecontrolsite_translateaccelerator, com.iolecontrolsite_translateaccelerator, ocidl/IOleControlSite::TranslateAccelerator
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
 - IOleControlSite::TranslateAccelerator
 - ocidl/IOleControlSite::TranslateAccelerator
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
 - IOleControlSite.TranslateAccelerator
---

# IOleControlSite::TranslateAccelerator


## -description

Passes a keystroke to the control site for processing.

## -parameters

### -param pMsg [in]

A pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure describing the keystroke to be processed.

### -param grfModifiers [in]

Flags describing the state of the Control, Alt, and Shift keys. The value of the flag can be any valid <a href="/previous-versions/windows/desktop/legacy/ms683763(v=vs.85)">KEYMODIFIERS</a> enumeration values.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The container processed the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The container did not process the message. This value must also be returned in all other error cases besides E_NOTIMPL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The container does not implement accelerator support.

</td>
</tr>
</table>

## -remarks

This method is called by a control that can be UI-active. In such cases, a control can process all keystrokes first through <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-translateaccelerator">IOleInPlaceActiveObject::TranslateAccelerator</a>, according to normal OLE Compound Document rules. Inside that method, the control can give the container certain messages to process first by calling <b>IOleControlSite::TranslateAccelerator</b> and using the return value to determine if any processing took place. Otherwise, the control always processes the message first. If the control does not use the keystroke as an accelerator, it passes the keystroke to the container through this method.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-translateaccelerator">IOleInPlaceActiveObject::TranslateAccelerator</a>