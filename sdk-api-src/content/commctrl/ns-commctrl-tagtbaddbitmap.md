---
UID: NS:commctrl.tagTBADDBITMAP
title: tagTBADDBITMAP
author: windows-sdk-content
description: Adds a bitmap that contains button images to a toolbar.
old-location: controls\TBADDBITMAP.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbaddbitmap.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPTBADDBITMAP, IDB_HIST_DISABLED, IDB_HIST_HOT, IDB_HIST_NORMAL, IDB_HIST_PRESSED, IDB_STD_LARGE_COLOR, IDB_STD_SMALL_COLOR, IDB_VIEW_LARGE_COLOR, IDB_VIEW_SMALL_COLOR, LPTBADDBITMAP, LPTBADDBITMAP structure pointer [Windows Controls], TBADDBITMAP, TBADDBITMAP structure [Windows Controls], _win32_TBADDBITMAP, _win32_TBADDBITMAP_cpp, commctrl/LPTBADDBITMAP, commctrl/TBADDBITMAP, controls.TBADDBITMAP, controls._win32_TBADDBITMAP, tagTBADDBITMAP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBADDBITMAP
product: Windows
targetos: Windows
req.typenames: TBADDBITMAP, *LPTBADDBITMAP
req.redist: 
---

# tagTBADDBITMAP structure


## -description


Adds a bitmap that contains button images to a toolbar.


## -struct-fields




### -field hInst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

If 
					<b>hInst</b> is <b>NULL</b>, set this member to the bitmap handle of the bitmap with the button images. Otherwise, set it to the resource identifier of the bitmap with the button images. 


## -remarks



If 
				<b>nID</b> holds a bitmap handle, rather than a resource ID, do not destroy the bitmap until it has been replaced with <a href="https://msdn.microsoft.com/en-us/library/Bb787391(v=VS.85).aspx">TB_REPLACEBITMAP</a>. Otherwise, the toolbar is destroyed.

Defined values can be used as indexes to the standard bitmaps. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb760433(v=VS.85).aspx">Toolbar Standard Button Image Index Values</a>.

The <b>TBADDBITMAP</b> structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb787289(v=VS.85).aspx">TB_ADDBITMAP</a> message.



