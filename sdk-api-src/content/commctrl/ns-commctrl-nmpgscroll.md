---
UID: NS:commctrl.NMPGSCROLL
title: NMPGSCROLL (commctrl.h)
description: Contains and receives information that the pager control uses when scrolling the contained window. It is used with the PGN_SCROLL notification.
helpviewer_keywords: ["*LPNMPGSCROLL","0","LPNMPGSCROLL","LPNMPGSCROLL structure pointer [Windows Controls]","NMPGSCROLL","NMPGSCROLL structure [Windows Controls]","PGF_SCROLLDOWN","PGF_SCROLLLEFT","PGF_SCROLLRIGHT","PGF_SCROLLUP","PGK_CONTROL","PGK_MENU","PGK_SHIFT","_win32_NMPGSCROLL","_win32_NMPGSCROLL_cpp","commctrl/LPNMPGSCROLL","commctrl/NMPGSCROLL","controls.NMPGSCROLL","controls._win32_NMPGSCROLL"]
old-location: controls\NMPGSCROLL.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\structures\nmpgscroll.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMPGSCROLL, 0, LPNMPGSCROLL, LPNMPGSCROLL structure pointer [Windows Controls], NMPGSCROLL, NMPGSCROLL structure [Windows Controls], PGF_SCROLLDOWN, PGF_SCROLLLEFT, PGF_SCROLLRIGHT, PGF_SCROLLUP, PGK_CONTROL, PGK_MENU, PGK_SHIFT, _win32_NMPGSCROLL, _win32_NMPGSCROLL_cpp, commctrl/LPNMPGSCROLL, commctrl/NMPGSCROLL, controls.NMPGSCROLL, controls._win32_NMPGSCROLL'
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
req.typenames: NMPGSCROLL, *LPNMPGSCROLL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNMPGSCROLL
 - commctrl/LPNMPGSCROLL
 - NMPGSCROLL
 - commctrl/NMPGSCROLL
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
 - NMPGSCROLL
---

# NMPGSCROLL structure


## -description

Contains and receives information that the pager control uses when scrolling the contained window. It is used with the <a href="/windows/desktop/Controls/pgn-scroll">PGN_SCROLL</a> notification.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification.

### -field fwKeys

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Modifier keys that are down when the scroll occurs. This can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
None of the modifier keys are down. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGK_SHIFT"></a><a id="pgk_shift"></a><dl>
<dt><b>PGK_SHIFT</b></dt>
</dl>
</td>
<td width="60%">
The SHIFT key is down. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGK_CONTROL"></a><a id="pgk_control"></a><dl>
<dt><b>PGK_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
The CONTROL key is down. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGK_MENU"></a><a id="pgk_menu"></a><dl>
<dt><b>PGK_MENU</b></dt>
</dl>
</td>
<td width="60%">
The ALT key is down. 

</td>
</tr>
</table>

### -field rcParent

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

Contains the client rectangle of the pager control.

### -field iDir

Type: <b>int</b>

Value that indicates in which direction the scroll is occurring. This will be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PGF_SCROLLDOWN"></a><a id="pgf_scrolldown"></a><dl>
<dt><b>PGF_SCROLLDOWN</b></dt>
</dl>
</td>
<td width="60%">
The contained window is being scrolled down. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGF_SCROLLLEFT"></a><a id="pgf_scrollleft"></a><dl>
<dt><b>PGF_SCROLLLEFT</b></dt>
</dl>
</td>
<td width="60%">
The contained window is being scrolled to the left. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGF_SCROLLRIGHT"></a><a id="pgf_scrollright"></a><dl>
<dt><b>PGF_SCROLLRIGHT</b></dt>
</dl>
</td>
<td width="60%">
The contained window is being scrolled to the right. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGF_SCROLLUP"></a><a id="pgf_scrollup"></a><dl>
<dt><b>PGF_SCROLLUP</b></dt>
</dl>
</td>
<td width="60%">
The contained window is being scrolled up. 

</td>
</tr>
</table>

### -field iXpos

Type: <b>int</b>

Contains the horizontal scroll position of the contained window, in pixels, before the scroll action.

### -field iYpos

Type: <b>int</b>

Contains the vertical scroll position of the contained window, in pixels, before the scroll action.

### -field iScroll

Type: <b>int</b>

On entry, contains the default scroll delta in pixels. This member can be modified to contain a different scroll delta amount if desired. This value is always positive, regardless of the scroll direction.

