---
UID: NF:oleidl.IOleInPlaceFrame.SetStatusText
title: IOleInPlaceFrame::SetStatusText (oleidl.h)
description: Sets and displays status text about the in-place object in the container's frame window status line.
helpviewer_keywords: ["IOleInPlaceFrame interface [COM]","SetStatusText method","IOleInPlaceFrame.SetStatusText","IOleInPlaceFrame::SetStatusText","SetStatusText","SetStatusText method [COM]","SetStatusText method [COM]","IOleInPlaceFrame interface","_ole_ioleinplaceframe_setstatustext","com.ioleinplaceframe_setstatustext","oleidl/IOleInPlaceFrame::SetStatusText"]
old-location: com\ioleinplaceframe_setstatustext.htm
tech.root: com
ms.assetid: e857bdbe-5510-4e35-ba73-d52b239e5b77
ms.date: 12/05/2018
ms.keywords: IOleInPlaceFrame interface [COM],SetStatusText method, IOleInPlaceFrame.SetStatusText, IOleInPlaceFrame::SetStatusText, SetStatusText, SetStatusText method [COM], SetStatusText method [COM],IOleInPlaceFrame interface, _ole_ioleinplaceframe_setstatustext, com.ioleinplaceframe_setstatustext, oleidl/IOleInPlaceFrame::SetStatusText
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
 - IOleInPlaceFrame::SetStatusText
 - oleidl/IOleInPlaceFrame::SetStatusText
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
 - IOleInPlaceFrame.SetStatusText
---

# IOleInPlaceFrame::SetStatusText


## -description

Sets and displays status text about the in-place object in the container's frame window status line.

## -parameters

### -param pszStatusText [in]

The message to be displayed.

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
<dt><b>S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
Some text was displayed but the message was too long and was truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

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
You should call <b>IOleInPlaceFrame::SetStatusText</b> when you need to ask the container to display object text in its frame's status line, if it has one. Because the container's frame window owns the status line, calling <b>IOleInPlaceFrame::SetStatusText</b> is the only way an object can display status information in the container's frame window. If the container refuses the object's request, the object application can, however, negotiate for border space to display its own status window.

When switching between menus owned by the container and the in-place active object, the status bar text is not reflected properly if the object does not call the container's <b>IOleInPlaceFrame::SetStatusText</b> method. For example, if, during an in-place session, the user were to select the <b>File</b> menu, the status bar would reflect the action that would occur if the user selected this menu. If the user then selects the <b>Edit</b> menu (which is owned by the in-place object), the status bar text would not change unless the <b>IOleInPlaceFrame::SetStatusText</b> happened to be called. This is because there is no way for the container to recognize that one of the object's menus has been made active because all the messages that the container would trap are now going to the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
To avoid potential problems, all objects being activated in place should process the <a href="/windows/desktop/menurc/wm-menuselect">WM_MENUSELECT</a> message and call <b>IOleInPlaceFrame::SetStatusText</b>, even if the object does not usually provide status information (in which case the object can just pass a <b>NULL</b> string for the requested status text).

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceFrame::SetStatusText</b>, do not make calls to the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-getborder">IOleInPlaceUIWindow::GetBorder</a>.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>