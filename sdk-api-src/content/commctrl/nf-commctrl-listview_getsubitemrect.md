---
UID: NF:commctrl.ListView_GetSubItemRect
title: ListView_GetSubItemRect macro
author: windows-sdk-content
description: Gets information about the rectangle that surrounds a subitem in a list-view control.
old-location: controls\ListView_GetSubItemRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getsubitemrect.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: LVIR_BOUNDS, LVIR_ICON, LVIR_LABEL, ListView_GetSubItemRect, ListView_GetSubItemRect macro [Windows Controls], _win32_ListView_GetSubItemRect, _win32_ListView_GetSubItemRect_cpp, commctrl/ListView_GetSubItemRect, controls.ListView_GetSubItemRect, controls._win32_ListView_GetSubItemRect
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetSubItemRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetSubItemRect macro


## -description


Gets information about the rectangle that surrounds a subitem in a list-view control. You can use this macro (recommended) or send the <a href="https://msdn.microsoft.com/985876b2-6eb3-4c96-88ea-ddec67ef5b5a">LVM_GETSUBITEMRECT</a> message explicitly. This macro is intended to be used only on list-view controls that use the <a href="List_view_window_styles.htm">LVS_REPORT</a> style. 


## -parameters




### -param hwnd

TBD


### -param iItem

Type: <b>int</b>

The index of the subitem's parent item. 


### -param iSubItem

Type: <b>int</b>

The one-based index of the subitem. 


### -param code

Type: <b>int</b>

A portion of the list-view subitem for which to retrieve the bounding rectangle information. This value can be one of the following: 

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
Returns the bounding rectangle of the entire item, including the icon and label. This is identical to LVIR_BOUNDS.

</td>
</tr>
</table>
 


### -param prc

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - lpRect

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the subitem bounding rectangle information. 

