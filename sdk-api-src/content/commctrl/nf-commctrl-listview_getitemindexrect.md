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

# ListView_GetItemIndexRect macro


## -description


Gets the bounding rectangle for all or part of a subitem in the current view of a specified list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/17704d24-c029-4d41-b198-04d1e78698e0">LVM_GETITEMINDEXRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param plvii [in]

Type: <b><a href="https://msdn.microsoft.com/62d28e14-fa0d-42c8-9f8e-afc0cfdff3e3">LVITEMINDEX</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/62d28e14-fa0d-42c8-9f8e-afc0cfdff3e3">LVITEMINDEX</a> structure for the parent item of the subitem. The caller is responsible for allocating this structure and setting its members. <i>plvii</i> must not be <b>NULL</b>.


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



