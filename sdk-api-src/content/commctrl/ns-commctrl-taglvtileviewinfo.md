---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagLVTILEVIEWINFO structure


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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a></b>

Size of an individual tile. Values for dimensions not specified as fixed in <b>dwFlags</b> are ignored.


### -field cLines

Type: <b>int</b>

Maximum number of text lines in each item label, not counting the title.


### -field rcLabelMargin

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> that contains coordinates of the label margin.


## -remarks



By default, the dimensions of tiles are determined automatically. To apply a fixed size, supply the correct value or values in <b>sizeTile</b> and set the appropriate flag in <b>dwFlags</b>. Allow enough vertical space for all lines of the label to be displayed. If a line does not fit in the allowed horizontal space, it is terminated with an ellipsis.
	




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8cd26367-7af8-4838-b2cf-815eba2b29f3">ListView_GetTileViewInfo</a>



<a href="https://msdn.microsoft.com/f4abf330-edce-49e3-a84c-cce2afd8a489">ListView_SetTileViewInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6953cdfc-8c59-4c6d-8998-f828cea3a315">Using List-View Controls</a>
 

 

