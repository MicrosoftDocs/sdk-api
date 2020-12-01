---
UID: NS:winuser.tagTRACKMOUSEEVENT
title: TRACKMOUSEEVENT (winuser.h)
description: Used by the TrackMouseEvent function to track when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
helpviewer_keywords: ["*LPTRACKMOUSEEVENT","LPTRACKMOUSEEVENT","LPTRACKMOUSEEVENT structure pointer [Keyboard and Mouse Input]","TME_CANCEL","TME_HOVER","TME_LEAVE","TME_NONCLIENT","TME_QUERY","TRACKMOUSEEVENT","TRACKMOUSEEVENT structure [Keyboard and Mouse Input]","_win32_TRACKMOUSEEVENT_str","_win32_trackmouseevent_str_cpp","inputdev.trackmouseevent_str","winui._win32_trackmouseevent_str","winuser/LPTRACKMOUSEEVENT","winuser/TRACKMOUSEEVENT"]
old-location: inputdev\trackmouseevent_str.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputstructures\trackmouseevent.htm
ms.date: 12/05/2018
ms.keywords: '*LPTRACKMOUSEEVENT, LPTRACKMOUSEEVENT, LPTRACKMOUSEEVENT structure pointer [Keyboard and Mouse Input], TME_CANCEL, TME_HOVER, TME_LEAVE, TME_NONCLIENT, TME_QUERY, TRACKMOUSEEVENT, TRACKMOUSEEVENT structure [Keyboard and Mouse Input], _win32_TRACKMOUSEEVENT_str, _win32_trackmouseevent_str_cpp, inputdev.trackmouseevent_str, winui._win32_trackmouseevent_str, winuser/LPTRACKMOUSEEVENT, winuser/TRACKMOUSEEVENT'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TRACKMOUSEEVENT, *LPTRACKMOUSEEVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTRACKMOUSEEVENT
 - winuser/tagTRACKMOUSEEVENT
 - LPTRACKMOUSEEVENT
 - winuser/LPTRACKMOUSEEVENT
 - TRACKMOUSEEVENT
 - winuser/TRACKMOUSEEVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - TRACKMOUSEEVENT
---

# TRACKMOUSEEVENT structure


## -description

Used by the <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> function to track when the mouse pointer leaves a window or hovers over a window for a specified amount of time.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the <b>TRACKMOUSEEVENT</b> structure, in bytes.

### -field dwFlags

Type: <b>DWORD</b>

The services requested. This member can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TME_CANCEL"></a><a id="tme_cancel"></a><dl>
<dt><b>TME_CANCEL</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The caller wants to cancel a prior tracking request. The caller should also specify the type of tracking that it wants to cancel. For example, to cancel hover tracking, the caller must pass the <b>TME_CANCEL</b> and <b>TME_HOVER</b> flags.

</td>
</tr>
<tr>
<td width="40%"><a id="TME_HOVER"></a><a id="tme_hover"></a><dl>
<dt><b>TME_HOVER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The caller wants hover notification. Notification is delivered as a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message. 

If the caller requests hover tracking while hover tracking is already active, the hover timer will be reset.

This flag is ignored if the mouse pointer is not over the specified window or area.

</td>
</tr>
<tr>
<td width="40%"><a id="TME_LEAVE"></a><a id="tme_leave"></a><dl>
<dt><b>TME_LEAVE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The caller wants leave notification. Notification is delivered as a <a href="/windows/desktop/inputdev/wm-mouseleave">WM_MOUSELEAVE</a> message. If the mouse is not over the specified window or area, a leave notification is generated immediately and no further tracking is performed.

</td>
</tr>
<tr>
<td width="40%"><a id="TME_NONCLIENT"></a><a id="tme_nonclient"></a><dl>
<dt><b>TME_NONCLIENT</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
 The caller wants hover and leave notification for the nonclient areas. Notification is delivered as <a href="/windows/desktop/inputdev/wm-ncmousehover">WM_NCMOUSEHOVER</a> and <a href="/windows/desktop/inputdev/wm-ncmouseleave">WM_NCMOUSELEAVE</a> messages.

</td>
</tr>
<tr>
<td width="40%"><a id="TME_QUERY"></a><a id="tme_query"></a><dl>
<dt><b>TME_QUERY</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The function fills in the structure instead of treating it as a tracking request. The structure is filled such that had that structure been passed to <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a>, it would generate the current tracking. The only anomaly is that the hover time-out returned is always the actual time-out and not <b>HOVER_DEFAULT</b>, if <b>HOVER_DEFAULT</b> was specified during the original <b>TrackMouseEvent</b> request.

</td>
</tr>
</table>

### -field hwndTrack

Type: <b>HWND</b>

A handle to the window to track.

### -field dwHoverTime

Type: <b>DWORD</b>

The hover time-out (if <b>TME_HOVER</b> was specified in <b>dwFlags</b>), in milliseconds. Can be <b>HOVER_DEFAULT</b>, which means to use the system default hover time-out.

## -remarks

The system default hover time-out is initially the menu drop-down time, which is 400 milliseconds. You can call <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> and use <b>SPI_GETMOUSEHOVERTIME</b> to retrieve the default hover time-out.

The system default hover rectangle is the same as the double-click rectangle. You can call <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> and use <b>SPI_GETMOUSEHOVERWIDTH</b> and <b>SPI_GETMOUSEHOVERHEIGHT</b> to retrieve the size of the rectangle within which the mouse pointer has to stay for <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent">TrackMouseEvent</a> to generate a <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> message.

## -see-also

<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>