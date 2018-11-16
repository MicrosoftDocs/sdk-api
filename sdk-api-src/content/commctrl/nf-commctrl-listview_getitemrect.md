---
UID: NF:commctrl.ListView_GetItemRect
title: ListView_GetItemRect macro
author: windows-sdk-content
description: Gets the bounding rectangle for all or part of an item in the current view. You can use this macro or send the LVM_GETITEMRECT message explicitly.
old-location: controls\ListView_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemrect.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LVIR_BOUNDS, LVIR_ICON, LVIR_LABEL, LVIR_SELECTBOUNDS, ListView_GetItemRect, ListView_GetItemRect macro [Windows Controls], _win32_ListView_GetItemRect, _win32_ListView_GetItemRect_cpp, commctrl/ListView_GetItemRect, controls.ListView_GetItemRect, controls._win32_ListView_GetItemRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - ListView_GetItemRect
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
- ListView_GetItemRect
: 
---

# ListView_GetItemRect macro


## -description


Gets the bounding rectangle for all or part of an item in the current view. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761049(v=VS.85).aspx">LVM_GETITEMRECT</a> message explicitly. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param i [in]

Type: <b>int</b>

The index of the list-view item. 


### -param prc [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the bounding rectangle. 


### -param code [in]

Type: <b>int</b>

The portion of the list-view item from which to retrieve the bounding rectangle. This parameter must be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIR_BOUNDS"></a><a id="lvir_bounds"></a><dl>
<dt><b>LVIR_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the entire item, including the icon and label.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_ICON"></a><a id="lvir_icon"></a><dl>
<dt><b>LVIR_ICON</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the icon or small icon.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_LABEL"></a><a id="lvir_label"></a><dl>
<dt><b>LVIR_LABEL</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the item text.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_SELECTBOUNDS"></a><a id="lvir_selectbounds"></a><dl>
<dt><b>LVIR_SELECTBOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Returns the union of the LVIR_ICON and LVIR_LABEL rectangles, but excludes columns in report view.

</td>
</tr>
</table>
 

