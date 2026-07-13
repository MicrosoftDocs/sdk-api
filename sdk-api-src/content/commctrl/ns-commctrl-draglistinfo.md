---
UID: NS:commctrl.tagDRAGLISTINFO
title: DRAGLISTINFO (commctrl.h)
description: Contains information about a drag event. The pointer to DRAGLISTINFO is passed as the lParam parameter of the drag list message.
helpviewer_keywords: ["*LPDRAGLISTINFO","DL_BEGINDRAG","DL_CANCELDRAG","DL_DRAGGING","DL_DROPPED","DRAGLISTINFO","DRAGLISTINFO structure [Windows Controls]","LPDRAGLISTINFO","LPDRAGLISTINFO structure pointer [Windows Controls]","_win32_DRAGLISTINFO","_win32_DRAGLISTINFO_cpp","commctrl/DRAGLISTINFO","commctrl/LPDRAGLISTINFO","controls.DRAGLISTINFO","controls._win32_DRAGLISTINFO"]
old-location: controls\DRAGLISTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\draglb\structures\draglistinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPDRAGLISTINFO, DL_BEGINDRAG, DL_CANCELDRAG, DL_DRAGGING, DL_DROPPED, DRAGLISTINFO, DRAGLISTINFO structure [Windows Controls], LPDRAGLISTINFO, LPDRAGLISTINFO structure pointer [Windows Controls], _win32_DRAGLISTINFO, _win32_DRAGLISTINFO_cpp, commctrl/DRAGLISTINFO, commctrl/LPDRAGLISTINFO, controls.DRAGLISTINFO, controls._win32_DRAGLISTINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DRAGLISTINFO, *LPDRAGLISTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDRAGLISTINFO
 - commctrl/tagDRAGLISTINFO
 - LPDRAGLISTINFO
 - commctrl/LPDRAGLISTINFO
 - DRAGLISTINFO
 - commctrl/DRAGLISTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - DRAGLISTINFO
---

# DRAGLISTINFO structure


## -description

Contains information about a drag event. The pointer to <b>DRAGLISTINFO</b> is passed as the 
			<i>lParam</i> parameter of the drag list message.

## -struct-fields

### -field uNotification

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The notification code that specifies the type of drag event. This member can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DL_BEGINDRAG"></a><a id="dl_begindrag"></a><dl>
<dt><b>DL_BEGINDRAG</b></dt>
</dl>
</td>
<td width="60%">
The user has clicked the left mouse button on a list item.

</td>
</tr>
<tr>
<td width="40%"><a id="DL_CANCELDRAG"></a><a id="dl_canceldrag"></a><dl>
<dt><b>DL_CANCELDRAG</b></dt>
</dl>
</td>
<td width="60%">
The user has canceled the drag operation by clicking the right mouse button or pressing the ESC key.

</td>
</tr>
<tr>
<td width="40%"><a id="DL_DRAGGING"></a><a id="dl_dragging"></a><dl>
<dt><b>DL_DRAGGING</b></dt>
</dl>
</td>
<td width="60%">
The user has moved the mouse while dragging an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="DL_DROPPED"></a><a id="dl_dropped"></a><dl>
<dt><b>DL_DROPPED</b></dt>
</dl>
</td>
<td width="60%">
The user has released the left mouse button, completing a drag operation.

</td>
</tr>
</table>

### -field hWnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the drag list box.

### -field ptCursor

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the current x- and y-coordinates of the mouse cursor.