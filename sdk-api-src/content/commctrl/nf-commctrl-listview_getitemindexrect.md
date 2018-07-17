---
UID: NF:commctrl.ListView_GetItemIndexRect
title: ListView_GetItemIndexRect macro
author: windows-sdk-content
description: Gets the bounding rectangle for all or part of a subitem in the current view of a specified list-view control. Use this macro or send the LVM_GETITEMINDEXRECT message explicitly.
old-location: controls\ListView_GetItemIndexRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemindexrect.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: LVIR_BOUNDS, LVIR_ICON, LVIR_LABEL, ListView_GetItemIndexRect, ListView_GetItemIndexRect macro [Windows Controls], _shell_ListView_GetItemIndexRect, _shell_ListView_GetItemIndexRect_cpp, commctrl/ListView_GetItemIndexRect, controls.ListView_GetItemIndexRect, controls._shell_ListView_GetItemIndexRect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetItemIndexRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetItemIndexRect macro


## -description


Gets the bounding rectangle for all or part of a subitem in the current view of a specified list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761046(v=VS.85).aspx">LVM_GETITEMINDEXRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param plvii [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb774762(v=VS.85).aspx">LVITEMINDEX</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/Bb774762(v=VS.85).aspx">LVITEMINDEX</a> structure for the parent item of the subitem. The caller is responsible for allocating this structure and setting its members. <i>plvii</i> must not be <b>NULL</b>.


### -param iSubItem [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The index of the subitem.


### -param code [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The portion of the list-view subitem for which to retrieve the bounding rectangle. This parameter must be one of the following values. 

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
Returns the bounding rectangle of the entire subitem, including the icon and label.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_ICON"></a><a id="lvir_icon"></a><dl>
<dt><b>LVIR_ICON</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the icon or small icon of the subitem.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_LABEL"></a><a id="lvir_label"></a><dl>
<dt><b>LVIR_LABEL</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the subitem text.

</td>
</tr>
</table>
 


### -param prc [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure to receive the coordinates. The caller is responsible for allocating this structure. <i>prc</i> must not be <b>NULL</b>.


## -remarks



If <i>iSubItem</i> is zero, this macro returns the coordinates of the rectangle to the item pointed to by <i>plvii</i>. The value LVIR_SELECTBOUNDS for the parameter <i>code</i> is not supported.



