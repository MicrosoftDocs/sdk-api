---
UID: NS:commctrl.tagLVTILEVIEWINFO
title: LVTILEVIEWINFO (commctrl.h)
author: windows-sdk-content
description: Provides information about a list-view control when it is displayed in tile view.
old-location: controls\LVTILEVIEWINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvtileviewinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PLVTILEVIEWINFO, LVTILEVIEWINFO, LVTILEVIEWINFO structure [Windows Controls], LVTVIF_EXTENDED, PLVTILEVIEWINFO, PLVTILEVIEWINFO structure pointer [Windows Controls], commctrl/LVTILEVIEWINFO, commctrl/PLVTILEVIEWINFO, controls.LVTILEVIEWINFO, controls.inet_LVTILEVIEWINFO, inet_LVTILEVIEWINFO, inet_LVTILEVIEWINFO_cpp"
ms.topic: struct
f1_keywords: ["commctrl/LVTILEVIEWINFO"]
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
 - LVTILEVIEWINFO
product: Windows
targetos: Windows
req.typenames: LVTILEVIEWINFO, *PLVTILEVIEWINFO
req.redist: 
ms.custom: 19H1
---

# LVTILEVIEWINFO structure


## -description


Provides information about a list-view control when it is displayed in tile view.



## -struct-fields




### -field cbSize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the <b>LVTILEVIEWINFO</b> structure.


### -field dwMask

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Mask that determines which members are valid. This member may be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIM_TILESIZE</dt>
</dl>
</td>
<td width="60%">
<b>sizeTile</b> is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIM_COLUMNS</dt>
</dl>
</td>
<td width="60%">
<b>cLines</b> is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIM_LABELMARGIN</dt>
</dl>
</td>
<td width="60%">
<b>rcLabelMargin</b> is valid.

</td>
</tr>
</table>
 


### -field dwFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flags that determines how the tiles are sized in tile view. This member may be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIF_AUTOSIZE</dt>
</dl>
</td>
<td width="60%">
Size the tiles automatically.

</td>
</tr>
<tr>
<td width="40%"><a id="LVTVIF_EXTENDED"></a><a id="lvtvif_extended"></a><dl>
<dt><b>LVTVIF_EXTENDED</b></dt>
</dl>
</td>
<td width="60%">
This flag is not supported and should not be used.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIF_FIXEDWIDTH</dt>
</dl>
</td>
<td width="60%">
Apply a fixed width to the tiles.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIF_FIXEDHEIGHT</dt>
</dl>
</td>
<td width="60%">
Apply a fixed height to the tiles.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVTVIF_FIXEDSIZE</dt>
</dl>
</td>
<td width="60%">
Apply a fixed height and width to the tiles.

</td>
</tr>
</table>
 


### -field sizeTile

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd145106(v=vs.85)">SIZE</a></b>

Size of an individual tile. Values for dimensions not specified as fixed in <b>dwFlags</b> are ignored.


### -field cLines

Type: <b>int</b>

Maximum number of text lines in each item label, not counting the title.


### -field rcLabelMargin

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> that contains coordinates of the label margin.


## -remarks



By default, the dimensions of tiles are determined automatically. To apply a fixed size, supply the correct value or values in <b>sizeTile</b> and set the appropriate flag in <b>dwFlags</b>. Allow enough vertical space for all lines of the label to be displayed. If a line does not fit in the allowed horizontal space, it is terminated with an ellipsis.
	




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_gettileviewinfo">ListView_GetTileViewInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_settileviewinfo">ListView_SetTileViewInfo</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/using-list-view-controls">Using List-View Controls</a>
 

 

