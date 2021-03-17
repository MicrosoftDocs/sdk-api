---
UID: NS:commctrl.tagTBADDBITMAP
title: TBADDBITMAP (commctrl.h)
description: Adds a bitmap that contains button images to a toolbar.
helpviewer_keywords: ["*LPTBADDBITMAP","IDB_HIST_DISABLED","IDB_HIST_HOT","IDB_HIST_NORMAL","IDB_HIST_PRESSED","IDB_STD_LARGE_COLOR","IDB_STD_SMALL_COLOR","IDB_VIEW_LARGE_COLOR","IDB_VIEW_SMALL_COLOR","LPTBADDBITMAP","LPTBADDBITMAP structure pointer [Windows Controls]","TBADDBITMAP","TBADDBITMAP structure [Windows Controls]","_win32_TBADDBITMAP","_win32_TBADDBITMAP_cpp","commctrl/LPTBADDBITMAP","commctrl/TBADDBITMAP","controls.TBADDBITMAP","controls._win32_TBADDBITMAP"]
old-location: controls\TBADDBITMAP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbaddbitmap.htm
ms.date: 12/05/2018
ms.keywords: '*LPTBADDBITMAP, IDB_HIST_DISABLED, IDB_HIST_HOT, IDB_HIST_NORMAL, IDB_HIST_PRESSED, IDB_STD_LARGE_COLOR, IDB_STD_SMALL_COLOR, IDB_VIEW_LARGE_COLOR, IDB_VIEW_SMALL_COLOR, LPTBADDBITMAP, LPTBADDBITMAP structure pointer [Windows Controls], TBADDBITMAP, TBADDBITMAP structure [Windows Controls], _win32_TBADDBITMAP, _win32_TBADDBITMAP_cpp, commctrl/LPTBADDBITMAP, commctrl/TBADDBITMAP, controls.TBADDBITMAP, controls._win32_TBADDBITMAP'
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
req.typenames: TBADDBITMAP, *LPTBADDBITMAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTBADDBITMAP
 - commctrl/tagTBADDBITMAP
 - LPTBADDBITMAP
 - commctrl/LPTBADDBITMAP
 - TBADDBITMAP
 - commctrl/TBADDBITMAP
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
 - TBADDBITMAP
---

# TBADDBITMAP structure


## -description

Adds a bitmap that contains button images to a toolbar.

## -struct-fields

### -field hInst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the module instance with the executable file that contains a bitmap resource. To use bitmap handles instead of resource IDs, set this member to <b>NULL</b>. 

You can add the system-defined button bitmaps to the list by specifying HINST_COMMCTRL as the <b>hInst</b> member and one of the following values as the <b>nID</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDB_STD_LARGE_COLOR"></a><a id="idb_std_large_color"></a><dl>
<dt><b>IDB_STD_LARGE_COLOR</b></dt>
</dl>
</td>
<td width="60%">
Large, color standard bitmaps.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_STD_SMALL_COLOR"></a><a id="idb_std_small_color"></a><dl>
<dt><b>IDB_STD_SMALL_COLOR</b></dt>
</dl>
</td>
<td width="60%">
Small, color standard bitmaps.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_VIEW_LARGE_COLOR"></a><a id="idb_view_large_color"></a><dl>
<dt><b>IDB_VIEW_LARGE_COLOR</b></dt>
</dl>
</td>
<td width="60%">
Small large, color view bitmaps.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_VIEW_SMALL_COLOR"></a><a id="idb_view_small_color"></a><dl>
<dt><b>IDB_VIEW_SMALL_COLOR</b></dt>
</dl>
</td>
<td width="60%">
Small, color view bitmaps.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_HIST_NORMAL"></a><a id="idb_hist_normal"></a><dl>
<dt><b>IDB_HIST_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Windows Explorer travel buttons and favorites bitmaps in normal state.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_HIST_HOT"></a><a id="idb_hist_hot"></a><dl>
<dt><b>IDB_HIST_HOT</b></dt>
</dl>
</td>
<td width="60%">
Windows Explorer travel buttons and favorites bitmaps in hot state.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_HIST_DISABLED"></a><a id="idb_hist_disabled"></a><dl>
<dt><b>IDB_HIST_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Windows Explorer travel buttons and favorites bitmaps in disabled state.

</td>
</tr>
<tr>
<td width="40%"><a id="IDB_HIST_PRESSED"></a><a id="idb_hist_pressed"></a><dl>
<dt><b>IDB_HIST_PRESSED</b></dt>
</dl>
</td>
<td width="60%">
Windows Explorer travel buttons and favorites bitmaps in pressed state.

</td>
</tr>
</table>

### -field nID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT_PTR</a></b>

If 
					<b>hInst</b> is <b>NULL</b>, set this member to the bitmap handle of the bitmap with the button images. Otherwise, set it to the resource identifier of the bitmap with the button images.

## -remarks

If 
				<b>nID</b> holds a bitmap handle, rather than a resource ID, do not destroy the bitmap until it has been replaced with <a href="/windows/desktop/Controls/tb-replacebitmap">TB_REPLACEBITMAP</a>. Otherwise, the toolbar is destroyed.

Defined values can be used as indexes to the standard bitmaps. For more information, see <a href="/windows/desktop/Controls/toolbar-standard-button-image-index-values">Toolbar Standard Button Image Index Values</a>.

The <b>TBADDBITMAP</b> structure is used with the <a href="/windows/desktop/Controls/tb-addbitmap">TB_ADDBITMAP</a> message.