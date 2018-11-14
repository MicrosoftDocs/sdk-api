---
UID: NF:commctrl.ListView_InsertItem
title: ListView_InsertItem macro
author: windows-sdk-content
description: Inserts a new item in a list-view control. You can use this macro or send the LVM_INSERTITEM message explicitly.
old-location: controls\ListView_InsertItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertitem.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_InsertItem, ListView_InsertItem macro [Windows Controls], _win32_ListView_InsertItem, _win32_ListView_InsertItem_cpp, commctrl/ListView_InsertItem, controls.ListView_InsertItem, controls._win32_ListView_InsertItem
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
 - ListView_InsertItem
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
- ListView_InsertItem
: 
---

# ListView_InsertItem macro


## -description


Inserts a new item in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/ac283e81-5b9f-4a90-acdb-fd7813c9cb84">LVM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pitem

Type: <b>const LPLVITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure that specifies the attributes of the list-view item. Use the <b>iItem</b> member to specify the zero-based index at which the new item should be inserted. If this value is greater than the number of items currently contained by the listview control, the new item will be appended to the end of the list and assigned the correct index. Examine the macro's return value to determine the actual index assigned to the item. 


## -remarks



You cannot use <b>ListView_InsertItem</b> or <a href="https://msdn.microsoft.com/ac283e81-5b9f-4a90-acdb-fd7813c9cb84">LVM_INSERTITEM</a> to insert subitems. The <b>iSubItem</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure must be zero. See <a href="https://msdn.microsoft.com/f1189b5d-bce7-4569-b4b9-bd750d7ef505">LVM_SETITEM</a> for information on setting subitems.

If a list-view control has the <a href="Extended_list_view_styles.htm">LVS_EX_CHECKBOXES</a> style set, any value placed in bits 12 through 15 of the <b>state</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure will be ignored. When an item is added with this style set, it will always be set to the unchecked state.

If a list-view control has either the <a href="List_view_window_styles.htm">LVS_SORTASCENDING</a> or <a href="List_view_window_styles.htm">LVS_SORTDESCENDING</a> window style, an <a href="https://msdn.microsoft.com/ac283e81-5b9f-4a90-acdb-fd7813c9cb84">LVM_INSERTITEM</a> message will fail if you try to insert an item that has LPSTR_TEXTCALLBACK as the <b>pszText</b> member of its <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure. 

The <b>ListView_InsertItem</b> macro will insert the new item in the proper position in the sort order if the following conditions hold: 

<ul>
<li>You are using one of the LVS_SORTXXX styles. </li>
<li>You are not using the LVS_OWNERDRAW style. </li>
<li>The 
						<b>pszText</b> member of the structure pointed to by <i>pitem</i> is not set to LPSTR_TEXTCALLBACK. </li>
</ul>


