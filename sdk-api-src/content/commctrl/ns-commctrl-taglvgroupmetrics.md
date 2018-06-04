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

# tagLVGROUPMETRICS structure


## -description


Contains information about the display of groups in a list-view control.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the <b>LVGROUPMETRICS</b> structure.


### -field mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that specify which members contain or are to receive valid data. Can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_BORDERCOLOR</dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_BORDERSIZE</dt>
</dl>
</td>
<td width="60%">
The <b>Left</b>, <b>Top</b>, <b>Right</b>, and <b>Bottom</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_NONE</dt>
</dl>
</td>
<td width="60%">
No members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_TEXTCOLOR</dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 


### -field Left

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the width of the left border in icon, small icon, or tile view.


### -field Top

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the width of the top border in all group views.


### -field Right

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the width of the right border in icon, small icon, or tile view.


### -field Bottom

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the width of the bottom border in all group views.


### -field crLeft

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the left border. Not implemented.


### -field crTop

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the top border. Not implemented.


### -field crRight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the right border. Not implemented.


### -field crBottom

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the bottom border. Not implemented.


### -field crHeader

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the header text. Not implemented.


### -field crFooter

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the footer text. Not implemented.


## -remarks



The width of a border determines the margins of the area within which items are placed. The top border is highlighted when the user moves the cursor over it, and when the user clicks on this border in a list that allows multiple selection, all items in the group are selected. 
	




## -see-also




<a href="https://msdn.microsoft.com/75e7da66-50c6-4834-ae66-e43b8f9b0b34">LVM_GETGROUPMETRICS</a>



<a href="https://msdn.microsoft.com/268b478d-da1f-4efe-9ee9-af3f12e089ee">LVM_SETGROUPMETRICS</a>



<a href="https://msdn.microsoft.com/dea34509-b785-4e45-a11a-d0a2e157b6d0">ListView_GetGroupMetrics</a>



<a href="https://msdn.microsoft.com/236799ba-3049-4bf8-ae28-0b1a064d3587">ListView_SetGroupMetrics</a>



<b>Reference</b>
 

 

