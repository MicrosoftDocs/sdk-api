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

# ListView_GetGroupRect macro


## -description


Gets the rectangle for a specified group. Use this macro or send the <a href="https://msdn.microsoft.com/9441a6c5-11d8-4f52-80dd-1b60befd9b9d">LVM_GETGROUPRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param iGroupId [in]

Type: <b>int</b>

Specifies the group by <b>iGroupId</b> (see <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a> structure).


### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Specifies the type of rectangle to retrieve. This parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVGGR_GROUP"></a><a id="lvggr_group"></a><dl>
<dt><b>LVGGR_GROUP</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the entire expanded group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGGR_HEADER"></a><a id="lvggr_header"></a><dl>
<dt><b>LVGGR_HEADER</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the header only (collapsed group).

</td>
</tr>
<tr>
<td width="40%"><a id="LVGGR_LABEL"></a><a id="lvggr_label"></a><dl>
<dt><b>LVGGR_LABEL</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the label only.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGGR_SUBSETLINK"></a><a id="lvggr_subsetlink"></a><dl>
<dt><b>LVGGR_SUBSETLINK</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the subset link only (markup subset). A list-view control can limit the number of visible items displayed in each group.  A link is presented to the user to allow the user to expand the group.  This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS_SUBSETED, see structure <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a>, member <b>state</b>). This flag is provided so that accessibility applications can locate the link.

</td>
</tr>
</table>
 


### -param prc [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure to receive information on the group specified by <i>iGroupId</i>. The message receiver is responsible for setting the structure members with information for the group specified by <i>iGroupId</i>. The calling application is responsible for allocating memory for the structure. 


