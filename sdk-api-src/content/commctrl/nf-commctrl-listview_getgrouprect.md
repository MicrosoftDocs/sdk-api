---
UID: NF:commctrl.ListView_GetGroupRect
title: ListView_GetGroupRect macro
author: windows-sdk-content
description: Gets the rectangle for a specified group. Use this macro or send the LVM_GETGROUPRECT message explicitly.
old-location: controls\ListView_GetGroupRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgrouprect.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LVGGR_GROUP, LVGGR_HEADER, LVGGR_LABEL, LVGGR_SUBSETLINK, ListView_GetGroupRect, ListView_GetGroupRect macro [Windows Controls], _shell_ListView_GetGroupRect, _shell_ListView_GetGroupRect_cpp, commctrl/ListView_GetGroupRect, controls.ListView_GetGroupRect, controls._shell_ListView_GetGroupRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ListView_GetGroupRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_GetGroupRect
: 
---

# ListView_GetGroupRect macro


## -description


Gets the rectangle for a specified group. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774935(v=VS.85).aspx">LVM_GETGROUPRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control.


### -param iGroupId [in]

Type: <b>int</b>

Specifies the group by <b>iGroupId</b> (see <a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a> structure).


### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LONG</a></b>

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
 Coordinates of the subset link only (markup subset). A list-view control can limit the number of visible items displayed in each group.  A link is presented to the user to allow the user to expand the group.  This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS_SUBSETED, see structure <a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a>, member <b>state</b>). This flag is provided so that accessibility applications can locate the link.

</td>
</tr>
</table>
 


### -param prc [in, out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure to receive information on the group specified by <i>iGroupId</i>. The message receiver is responsible for setting the structure members with information for the group specified by <i>iGroupId</i>. The calling application is responsible for allocating memory for the structure. 


