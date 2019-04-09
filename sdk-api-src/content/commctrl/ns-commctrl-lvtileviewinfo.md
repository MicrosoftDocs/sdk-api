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
---

# LVTILEVIEWINFO structure


## -description


Provides information about a list-view control when it is displayed in tile view.



## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the <b>LVTILEVIEWINFO</b> structure.


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a></b>

Size of an individual tile. Values for dimensions not specified as fixed in <b>dwFlags</b> are ignored.


### -field cLines

Type: <b>int</b>

Maximum number of text lines in each item label, not counting the title.


### -field rcLabelMargin

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> that contains coordinates of the label margin.


## -remarks



By default, the dimensions of tiles are determined automatically. To apply a fixed size, supply the correct value or values in <b>sizeTile</b> and set the appropriate flag in <b>dwFlags</b>. Allow enough vertical space for all lines of the label to be displayed. If a line does not fit in the allowed horizontal space, it is terminated with an ellipsis.
	




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb775012(v=VS.85).aspx">ListView_GetTileViewInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775120(v=VS.85).aspx">ListView_SetTileViewInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774736(v=VS.85).aspx">Using List-View Controls</a>
 

 

