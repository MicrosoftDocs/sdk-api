---
UID: NS:commctrl.tagLVGROUPMETRICS
title: tagLVGROUPMETRICS
author: windows-sdk-content
description: Contains information about the display of groups in a list-view control.
old-location: controls\LVGROUPMETRICS.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvgroupmetrics.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PLVGROUPMETRICS, LVGROUPMETRICS, LVGROUPMETRICS structure [Windows Controls], PLVGROUPMETRICS, PLVGROUPMETRICS structure pointer [Windows Controls], commctrl/LVGROUPMETRICS, commctrl/PLVGROUPMETRICS, controls.LVGROUPMETRICS, controls.inet_LVGROUPMETRICS, inet_LVGROUPMETRICS, inet_LVGROUPMETRICS_cpp, tagLVGROUPMETRICS"
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
 - LVGROUPMETRICS
product: Windows
targetos: Windows
req.typenames: LVGROUPMETRICS, *PLVGROUPMETRICS
req.redist: 
---

# tagLVGROUPMETRICS structure


## -description


Contains information about the display of groups in a list-view control.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Size of the <b>LVGROUPMETRICS</b> structure.


### -field mask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Specifies the width of the left border in icon, small icon, or tile view.


### -field Top

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Specifies the width of the top border in all group views.


### -field Right

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Specifies the width of the right border in icon, small icon, or tile view.


### -field Bottom

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

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




<a href="https://msdn.microsoft.com/en-us/library/Bb774934(v=VS.85).aspx">LVM_GETGROUPMETRICS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761168(v=VS.85).aspx">LVM_SETGROUPMETRICS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761284(v=VS.85).aspx">ListView_GetGroupMetrics</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775080(v=VS.85).aspx">ListView_SetGroupMetrics</a>



<b>Reference</b>
 

 

