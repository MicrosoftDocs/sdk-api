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

# _tableRowParms structure


## -description


Defines the attributes of rows in a table. The definitions include the corresponding Rich Text Format (RTF) control words, which are defined in the <a href="http://go.microsoft.com/fwlink/p/?linkid=239794">Rich Text Format (RTF) Specification</a>. 



## -struct-fields




### -field cbRow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The count of bytes in this structure.


### -field cbCell

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The count of bytes in <a href="https://msdn.microsoft.com/75bf07bd-103b-4f35-b421-5a7559c7b90e">TABLECELLPARMS</a>.


### -field cCell

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The count of cells in a row, up to the maximum specified by MAX_TABLE_CELLS.


### -field cRow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The count of rows.


### -field dxCellMargin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The size of the left and right margins in a cell (\trgaph).


### -field dxIndent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The amount of left indentation, or right indentation if the <b>fRTL</b> member is <b>TRUE</b> (similar to \trleft).


### -field dyHeight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The height of a row (\trrh). 


### -field nAlignment

 


### -field fRTL

 


### -field fKeep

 


### -field fKeepFollow

 


### -field fWrap

 


### -field fIdentCells

 


### -field cpStartRow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The character position that indicates where to insert table. A value of –1 indicates the character position of the selection. 


### -field bTableLevel

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The table nesting level (<a href="https://msdn.microsoft.com/36ADA41B-735B-4D6E-92B1-33260C71DF73">EM_GETTABLEPARMS</a> only).


### -field iCell

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The index of the cell to insert or delete (<a href="https://msdn.microsoft.com/6CE9B8D1-68C9-4692-8454-24BC81E9038F">EM_SETTABLEPARMS</a> only).


#### - fIdentCells:1

Type: <b>DWORD</b>

 Indent cells.


#### - fKeep:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Keep rows together (\trkeep).


#### - fKeepFollow:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Keep the row on the same page as the following row (\trkeepfollow).


#### - fRTL:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Display cells in right-to-left order (\rtlrow).


#### - fWrap:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Wrap text to the right or left, depending on <b>bAlignment</b>
							(see \tdfrmtxtLeftN and \tdfrmtxtRightN).


#### - nAlignment:3

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


Row alignment \trql, trqr, \trqc)



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFA_CENTER"></a><a id="pfa_center"></a><dl>
<dt><b>PFA_CENTER</b></dt>
</dl>
</td>
<td width="60%">
The rows are centered.

</td>
</tr>
<tr>
<td width="40%"><a id="PFA_LEFT"></a><a id="pfa_left"></a><dl>
<dt><b>PFA_LEFT</b></dt>
</dl>
</td>
<td width="60%">
The rows are aligned with the left margin.

</td>
</tr>
<tr>
<td width="40%"><a id="PFA_RIGHT"></a><a id="pfa_right"></a><dl>
<dt><b>PFA_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
The rows are aligned with the right margin.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/7F9B2F28-1035-44AA-9DF6-57BC62886A4E">EM_INSERTTABLE</a>



<a href="https://msdn.microsoft.com/75bf07bd-103b-4f35-b421-5a7559c7b90e">TABLECELLPARMS</a>
 

 

